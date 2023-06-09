---
layout: "page"
title: "DependentRequiredKeyword Class"
bookmark: "DependentRequiredKeyword"
permalink: "/api/JsonSchema.Net/:title/"
order: "9.01.15"
---
**Namespace:** Json.Schema

**Inheritance:**
`DependentRequiredKeyword`
 🡒 
`object`

**Implemented interfaces:**

- IJsonSchemaKeyword
- IEquatable\<DependentRequiredKeyword\>

Handles `dependentRequired`.

## Fields

| Name | Type | Summary |
|---|---|---|
| **Name** | string | The JSON name of the keyword. |

## Properties

| Name | Type | Summary |
|---|---|---|
| **Requirements** | IReadOnlyDictionary\<string, IReadOnlyList\<string\>\> | The collection of "required"-type dependencies. |

## Constructors

### DependentRequiredKeyword(IReadOnlyDictionary\<string, IReadOnlyList\<string\>\> values)

Creates a new **Json.Schema.DependentRequiredKeyword**.

#### Declaration

```c#
public DependentRequiredKeyword(IReadOnlyDictionary<string, IReadOnlyList<string>> values)
```

| Parameter | Type | Description |
|---|---|---|
| values | IReadOnlyDictionary\<string, IReadOnlyList\<string\>\> | The collection of "required"-type dependencies. |


## Methods

### Equals(DependentRequiredKeyword other)

Indicates whether the current object is equal to another object of the same type.

#### Declaration

```c#
public bool Equals(DependentRequiredKeyword other)
```

| Parameter | Type | Description |
|---|---|---|
| other | DependentRequiredKeyword | An object to compare with this object. |


#### Returns

true if the current object is equal to the <paramref name="other">other</paramref> parameter; otherwise, false.

### Equals(object obj)

Determines whether the specified object is equal to the current object.

#### Declaration

```c#
public override bool Equals(object obj)
```

| Parameter | Type | Description |
|---|---|---|
| obj | object | The object to compare with the current object. |


#### Returns

true if the specified object  is equal to the current object; otherwise, false.

### Evaluate(EvaluationContext context)

Performs evaluation for the keyword.

#### Declaration

```c#
public void Evaluate(EvaluationContext context)
```

| Parameter | Type | Description |
|---|---|---|
| context | EvaluationContext | Contextual details for the evaluation process. |


### GetHashCode()

Serves as the default hash function.

#### Declaration

```c#
public override int GetHashCode()
```


#### Returns

A hash code for the current object.

