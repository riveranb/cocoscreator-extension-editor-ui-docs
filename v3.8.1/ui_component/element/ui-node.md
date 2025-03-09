# UI Node Component

## Initialize

### Basic Usage

Basic node:
```html
<ui-node></ui-node>
```

### With Value

Node with UUID:
```html
<ui-node value="f46876e4-e81b-4931-b493-6d367be385e7"></ui-node>
```

### With Type

Node with specific type:
```html
<ui-node type="cc.Node"></ui-node>
```

### States

Disabled node:
```html
<ui-node disabled></ui-node>
```

Readonly node:
```html
<ui-node readonly></ui-node>
```

Invalid node:
```html
<ui-node invalid></ui-node>
```

Hidden node:
```html
<ui-node hidden></ui-node>
```

## Parameters

### Attributes
```typescript
value = ''; // node uuid
type = ''; // node type filter
disabled; // statement
readonly; // statement
invalid; // statement
hidden; // statement
```

## Events

### Available Events
```typescript
change // general case use this event
confirm
```

### Usage Examples

#### Vue.js
```html
<ui-node
    type="cc.Node"
    @change="onChange($event.target.value)"
    @confirm="onConfirm($event.target.value)"
></ui-node>
```

#### Vanilla JavaScript
```html
<ui-node id="node" type="cc.Node"></ui-node>
```

```javascript
const element = document.getElementById('#node');

// addEventListener
element.addEventListener('change', (event) => {
    // changed value
    console.log(event.target.value);
});
element.addEventListener('confirm', (event) => {
    // confirm value
    console.log(event.target.value);
});
```

## Get/Set Value
```javascript
const element = document.getElementById('#node');
// set value
element.value = 'f46876e4-e81b-4931-b493-6d367be385e7';

// get value
const uuid = element.value;
```

> **Note:** This is a built-in UI component for Cocos Creator Editor. It provides a node reference field for selecting nodes in the scene. 