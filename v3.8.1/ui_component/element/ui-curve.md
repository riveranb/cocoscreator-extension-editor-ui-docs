# UI Curve Component

## Initialize

### Value + Config Example

```html
<ui-curve value='{"preWrapMode":0,"postWrapMode":0,"keys":[{"outTangent":1,"point":{"x":0.2,"y":0.4},"interpMode":0,"tangentWeightMode":0,"outTangentWeight":1,"inTangentWeight":1,"inTangent":0},{"inTangent":1,"outTangent":1,"point":{"x":0.8,"y":0.8},"interpMode":0,"tangentWeightMode":0,"outTangentWeight":1,"inTangentWeight":1},{"inTangent":0.5,"point":{"x":1,"y":0.5},"interpMode":0,"tangentWeightMode":0,"outTangentWeight":1,"inTangentWeight":1,"outTangent":0}],"color":"red"}' config='{"xRange":[0,1],"yRange":[0,1],"precision":4,"showPreWrapMode":true,"showPostWrapMode":true,"type":"hermit"}'></ui-curve>
```

### Normal Curves

Multiple curve examples with different configurations:
```html
<ui-curve value='{"preWrapMode":0,"postWrapMode":0,"keys":[{"point":{"x":0,"y":0},"interpMode":1,"tangentWeightMode":0,"outTangentWeight":1,"inTangentWeight":1,"outTangent":0,"inTangent":0},{"point":{"x":0.5,"y":0.5},"interpMode":0,"tangentWeightMode":0,"outTangentWeight":1,"inTangentWeight":1,"outTangent":0,"inTangent":0},{"point":{"x":1,"y":1},"interpMode":0,"tangentWeightMode":0,"outTangentWeight":1,"inTangentWeight":1,"outTangent":0,"inTangent":0}],"color":"red"}' config='{"xRange":[0,1],"yRange":[0,1],"precision":4,"showPreWrapMode":true,"showPostWrapMode":true,"type":"hermit"}'></ui-curve>
```

### Negative Config

```html
<ui-curve value='{"preWrapMode":0,"postWrapMode":0,"keys":[{"point":{"x":0,"y":0},"interpMode":1,"tangentWeightMode":0,"outTangentWeight":1,"inTangentWeight":1,"outTangent":0,"inTangent":0},{"point":{"x":0.5,"y":0.5},"interpMode":0,"tangentWeightMode":0,"outTangentWeight":1,"inTangentWeight":1,"outTangent":0,"inTangent":0},{"point":{"x":1,"y":1},"interpMode":0,"tangentWeightMode":0,"outTangentWeight":1,"inTangentWeight":1,"outTangent":0,"inTangent":0}],"color":"red"}' config='{"xRange":[-1,1],"yRange":[-1,1],"negative":true,"precision":4,"showPreWrapMode":true,"showPostWrapMode":true,"type":"hermit"}'></ui-curve>
```

### States

Disabled curve:
```html
<ui-curve disabled></ui-curve>
```

Readonly curve:
```html
<ui-curve readonly></ui-curve>
```

Invalid data:
```html
<ui-curve value="test"></ui-curve>
```

Hidden curve:
```html
<ui-curve hidden></ui-curve>
```

## Parameters

### Attributes
```typescript
config // Configuration object for the curve
value // Curve data object
disabled
readonly
```

### Value Data Example
```json
{
    "preWrapMode": 0,
    "postWrapMode": 0,
    "keys": [
        {
            "outTangent": 1,
            "point": {
                "x": 0.2,
                "y": 0.4
            },
            "interpMode": 0,
            "tangentWeightMode": 0,
            "outTangentWeight": 1,
            "inTangentWeight": 1,
            "inTangent": 0
        },
        {
            "inTangent": 1,
            "outTangent": 1,
            "point": {
                "x": 0.8,
                "y": 0.8
            },
            "interpMode": 0,
            "tangentWeightMode": 0,
            "outTangentWeight": 1,
            "inTangentWeight": 1
        },
        {
            "inTangent": 0.5,
            "point": {
                "x": 1,
                "y": 0.5
            },
            "interpMode": 0,
            "tangentWeightMode": 0,
            "outTangentWeight": 1,
            "inTangentWeight": 1,
            "outTangent": 0
        }
    ],
    "color": "red"
}
```

### Config Data Example
```json
{
    "xRange": [0, 1],
    "yRange": [0, 1],
    "precision": 4,
    "showPreWrapMode": true,
    "showPostWrapMode": true,
    "type": "hermit"
}
```

> **Note:** This is a built-in UI component for Cocos Creator Editor. It provides an interactive curve editor for animation and other curve-based data. 