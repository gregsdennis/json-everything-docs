---
layout: "page"
title: "WriteOnlyKeywordJsonConverter Class"
bookmark: "WriteOnlyKeywordJsonConverter"
permalink: "/api/JsonSchema.Net/:title/"
order: "10.01.186"
---
**Namespace:** Json.Schema

**Inheritance:**
`WriteOnlyKeywordJsonConverter`
 🡒 
`WeaklyTypedJsonConverter<WriteOnlyKeyword>`
 🡒 
`JsonConverter<WriteOnlyKeyword>`
 🡒 
`JsonConverter`
 🡒 
`object`

**Implemented interfaces:**

- IWeaklyTypedJsonConverter

JSON converter for **Json.Schema.WriteOnlyKeyword**.

## Properties

| Name | Type | Summary |
|---|---|---|
| **HandleNull** | bool |  |
| **Type** | Type |  |

## Methods

### Read(ref Utf8JsonReader reader, Type typeToConvert, JsonSerializerOptions options)

Reads and converts the JSON to type **Json.Schema.WriteOnlyKeyword**.

#### Declaration

```c#
public override WriteOnlyKeyword Read(ref Utf8JsonReader reader, Type typeToConvert, JsonSerializerOptions options)
```

| Parameter | Type | Description |
|---|---|---|
| reader | ref Utf8JsonReader | The reader. |
| typeToConvert | Type | The type to convert. |
| options | JsonSerializerOptions | An object that specifies serialization options to use. |


#### Returns

The converted value.

### Write(Utf8JsonWriter writer, WriteOnlyKeyword value, JsonSerializerOptions options)

Writes a specified value as JSON.

#### Declaration

```c#
public override void Write(Utf8JsonWriter writer, WriteOnlyKeyword value, JsonSerializerOptions options)
```

| Parameter | Type | Description |
|---|---|---|
| writer | Utf8JsonWriter | The writer to write to. |
| value | WriteOnlyKeyword | The value to convert to JSON. |
| options | JsonSerializerOptions | An object that specifies serialization options to use. |


