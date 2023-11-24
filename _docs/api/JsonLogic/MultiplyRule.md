---
layout: "page"
title: "MultiplyRule Class"
bookmark: "MultiplyRule"
permalink: "/api/JsonLogic/:title/"
0.11.029"
---
**Namespace:** Json.Logic.Rules

**Inheritance:**
`MultiplyRule`
 🡒 
`Rule`
 🡒 
`object`

Handles the `*` operation.

## Methods

### Apply(JsonNode data, JsonNode contextData)

Applies the rule to the input data.

#### Declaration

```c#
public override JsonNode Apply(JsonNode data, JsonNode contextData)
```

| Parameter | Type | Description |
|---|---|---|
| data | JsonNode | The input data. |
| contextData | JsonNode | Optional secondary data.  Used by a few operators to pass a secondary     data context to inner operators. |


#### Returns

The result of the rule.

