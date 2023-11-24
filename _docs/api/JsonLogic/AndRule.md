---
layout: "page"
title: "AndRule Class"
bookmark: "AndRule"
permalink: "/api/JsonLogic/:title/"
0.11.002"
---
**Namespace:** Json.Logic.Rules

**Inheritance:**
`AndRule`
 🡒 
`Rule`
 🡒 
`object`

Handles the `and` operation.

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

