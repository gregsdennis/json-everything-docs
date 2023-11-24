---
layout: "page"
title: "JsonSchemaBuilderExtensions Class"
bookmark: "JsonSchemaBuilderExtensions"
permalink: "/api/JsonSchema.Net.Data/:title/"
0.02.004"
---
**Namespace:** Json.Schema.Data

**Inheritance:**
`JsonSchemaBuilderExtensions`
 🡒 
`object`

Provides a fluent interface for **Json.Schema.JsonSchemaBuilder**.

## Methods

### Data(this JsonSchemaBuilder builder, IReadOnlyDictionary\<string, string\> data)

Adds a `data` keyword.

#### Declaration

```c#
public static JsonSchemaBuilder Data(this JsonSchemaBuilder builder, IReadOnlyDictionary<string, string> data)
```

| Parameter | Type | Description |
|---|---|---|
| builder | JsonSchemaBuilder | The builder. |
| data | IReadOnlyDictionary\<string, string\> | The collection of keywords and references. |


#### Returns

The builder.

### Data(this JsonSchemaBuilder builder, params (string name, string reference)[] data)

Adds a `data` keyword.

#### Declaration

```c#
public static JsonSchemaBuilder Data(this JsonSchemaBuilder builder, params (string name, string reference)[] data)
```

| Parameter | Type | Description |
|---|---|---|
| builder | JsonSchemaBuilder | The builder. |
| data | params (string name, string reference)[] | The collection of keywords and references. |


#### Returns

The builder.

