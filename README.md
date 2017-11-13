# Proto.Serialization.Json

![NuGet Stats](https://img.shields.io/nuget/v/Proto.Serialization.Json.svg)

Serialization adapter for [Proto.Actor](http://proto.actor/) allowing to use `Newtonsoft.Json` for message serialization.
Please note, that using this makes remote communication with Proto.Actor less performant than using native `Google.Protobuf`.

The purpose of using JSON with Proto.Actor is faster prototyping and testing.

# Build

```shell
fake build
```
