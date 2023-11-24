---
layout: "page"
title: "ContentEncodingKeyword Class"
bookmark: "ContentEncodingKeyword"
permalink: "/api/JsonSchema.Net/:title/"
0.01.017"
---
**Namespace:** Json.Schema

**Inheritance:**
`ContentEncodingKeyword`
 🡒 
`object`

**Implemented interfaces:**

- IJsonSchemaKeyword

Handles `contentMediaEncoding`.

## Fields

| Name | Type | Summary |
|---|---|---|
| **Name** | string | The JSON name of the keyword. |

## Properties

| Name | Type | Summary |
|---|---|---|
| **Value** | string | The encoding value. |

## Constructors

### ContentEncodingKeyword(string value)

Creates a new **Json.Schema.ContentEncodingKeyword**.

#### Declaration

```c#
public ContentEncodingKeyword(string value)
```

| Parameter | Type | Description |
|---|---|---|
| value | string | The encoding value. |


## Methods

### GetConstraint(SchemaConstraint schemaConstraint, IReadOnlyList\<KeywordConstraint\> localConstraints, EvaluationContext context)

Builds a constraint object for a keyword.

#### Declaration

```c#
public KeywordConstraint GetConstraint(SchemaConstraint schemaConstraint, IReadOnlyList<KeywordConstraint> localConstraints, EvaluationContext context)
```

| Parameter | Type | Description |
|---|---|---|
| schemaConstraint | SchemaConstraint | The **Json.Schema.SchemaConstraint** for the schema object that houses this keyword. |
| localConstraints | IReadOnlyList\<KeywordConstraint\> | The set of other **Json.Schema.KeywordConstraint**s that have been processed prior to this one. Will contain the constraints for keyword dependencies. |
| context | EvaluationContext | The **Json.Schema.EvaluationContext**. |


#### Returns

A constraint object.

