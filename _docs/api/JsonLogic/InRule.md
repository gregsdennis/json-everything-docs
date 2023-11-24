---
layout: "page"
title: "InRule Class"
bookmark: "InRule"
permalink: "/api/JsonLogic/:title/"
0.11.008"
---
**Namespace:** Json.Logic.Rules

**Inheritance:**
`InRule`
 🡒 
`Rule`
 🡒 
`object`

Handles the `in` operation.

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

