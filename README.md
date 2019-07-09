# Proto.Serialization.Json

[![NuGet Stats](https://img.shields.io/nuget/v/Proto.Serialization.Json.svg)](https://www.nuget.org/packages/Proto.Serialization.Json/)

Serialization adapter for [Proto.Actor](http://proto.actor/) allowing to use `Newtonsoft.Json` for message serialization.
Please note, that using this makes remote communication with Proto.Actor less performant than using native `Google.Protobuf`.

The purpose of using JSON with Proto.Actor is faster prototyping and testing.

# Usage

```csharp
Serialization.RegisterSerializer(new NewtonsoftSerializer(), true);
```

It's worth to note that it requires type information to be stored in JSON, so when using your own `JsonSerializationSettings` use at least `TypeNameHandling.Auto`, but preferably `TypeNameHandling.All`:

```csharp
JsonSerializerSettings settings = new JsonSerializerSettings {
    TypeNameHandling = TypeNameHandling.All, // <-- here
};
Serialization.RegisterSerializer(new NewtonsoftSerializer(settings), true);
```

# Build

```shell
paket install
fake build
```
