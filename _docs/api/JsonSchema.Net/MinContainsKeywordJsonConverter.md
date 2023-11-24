---
layout: "page"
title: "MinContainsKeywordJsonConverter Class"
bookmark: "MinContainsKeywordJsonConverter"
permalink: "/api/JsonSchema.Net/:title/"
0.01.102"
---
**Namespace:** Json.Schema

**Inheritance:**
`MinContainsKeywordJsonConverter`
 🡒 
`JsonConverter<MinContainsKeyword>`
 🡒 
`JsonConverter`
 🡒 
`object`

JSON converter for **Json.Schema.MinContainsKeyword**.

## Properties

| Name | Type | Summary |
|---|---|---|
| **HandleNull** | bool |  |

## Methods

### Read(ref Utf8JsonReader reader, Type typeToConvert, JsonSerializerOptions options)

Reads and converts the JSON to type **Json.Schema.MinContainsKeyword**.

#### Declaration

```c#
public override MinContainsKeyword Read(ref Utf8JsonReader reader, Type typeToConvert, JsonSerializerOptions options)
```

| Parameter | Type | Description |
|---|---|---|
| reader | ref Utf8JsonReader | The reader. |
| typeToConvert | Type | The type to convert. |
| options | JsonSerializerOptions | An object that specifies serialization options to use. |


#### Returns

The converted value.

### Write(Utf8JsonWriter writer, MinContainsKeyword value, JsonSerializerOptions options)

Writes a specified value as JSON.

#### Declaration

```c#
public override void Write(Utf8JsonWriter writer, MinContainsKeyword value, JsonSerializerOptions options)
```

| Parameter | Type | Description |
|---|---|---|
| writer | Utf8JsonWriter | The writer to write to. |
| value | MinContainsKeyword | The value to convert to JSON. |
| options | JsonSerializerOptions | An object that specifies serialization options to use. |


