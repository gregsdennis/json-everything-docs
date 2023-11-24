---
layout: "page"
title: "JsonPointerJsonConverter Class"
bookmark: "JsonPointerJsonConverter"
permalink: "/api/JsonPointer.Net/:title/"
0.10.003"
---
**Namespace:** Json.Pointer

**Inheritance:**
`JsonPointerJsonConverter`
 🡒 
`JsonConverter<JsonPointer>`
 🡒 
`JsonConverter`
 🡒 
`object`

Converter for **Json.Pointer.JsonPointer**.

## Properties

| Name | Type | Summary |
|---|---|---|
| **HandleNull** | bool |  |

## Methods

### Read(ref Utf8JsonReader reader, Type typeToConvert, JsonSerializerOptions options)

Reads and converts the JSON to type **Json.Pointer.JsonPointer**.

#### Declaration

```c#
public override JsonPointer Read(ref Utf8JsonReader reader, Type typeToConvert, JsonSerializerOptions options)
```

| Parameter | Type | Description |
|---|---|---|
| reader | ref Utf8JsonReader | The reader. |
| typeToConvert | Type | The type to convert. |
| options | JsonSerializerOptions | An object that specifies serialization options to use. |


#### Returns

The converted value.

### Write(Utf8JsonWriter writer, JsonPointer value, JsonSerializerOptions options)

Writes a specified value as JSON.

#### Declaration

```c#
public override void Write(Utf8JsonWriter writer, JsonPointer value, JsonSerializerOptions options)
```

| Parameter | Type | Description |
|---|---|---|
| writer | Utf8JsonWriter | The writer to write to. |
| value | JsonPointer | The value to convert to JSON. |
| options | JsonSerializerOptions | An object that specifies serialization options to use. |


