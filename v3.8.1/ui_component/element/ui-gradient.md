# UI Gradient Component

## Initialize

### Basic Usage

```html
<ui-gradient></ui-gradient>
```

### With Value

```html
<ui-gradient value='{"alpha":[{"value":0,"progress":0},{"value":1,"progress":0.2},{"value":0,"progress":0.4},{"value":1,"progress":0.6},{"value":0,"progress":0.8},{"value":1,"progress":1}],"color":[{"value":"#000000","progress":0},{"value":"#909999","progress":0.5},{"value":"#102399","progress":1}]}'></ui-gradient>
```

### States

Readonly gradient:
```html
<ui-gradient readonly value='{"alpha":[{"value":0,"progress":0},{"value":1,"progress":1}]}'></ui-gradient>
```

Disabled gradient:
```html
<ui-gradient disabled value='{"alpha":[{"value":0,"progress":0},{"value":1,"progress":1}]}'></ui-gradient>
```

Invalid gradient:
```html
<ui-gradient invalid value="xxx"></ui-gradient>
```

Hidden gradient:
```html
<ui-gradient hidden></ui-gradient>
```

## Parameters

### Attributes
```typescript
value  // { "alpha":[{"value":0,"progress":0}], "color":[{"value":"#000000","progress":0}] }
disabled
readonly
invalid
hidden
```

## Events

### Available Events
```typescript
change
confirm // general case use this event
open
```

### Usage Examples

#### Vue.js
```html
<ui-gradient ref="gradient" value='{"alpha":[{"progress":0,"value":0},{"progress":1,"value":1}],"color":[{"progress":0.9174107142857143,"value":"#c93333"}]}'
    @confirm="onConfirm($event.target.value)"
    @change="onChange($event.target.value)"
    @open="onOpen"
></ui-gradient>
```

#### Vanilla JavaScript
```html
<ui-gradient id="gradient"></ui-gradient>
```

```javascript
const element = document.getElementById('#gradient');

element.addEventListener('confirm', (event) => {
    const colorObject = event.target.value;
});
element.addEventListener('change', (event) => {
    console.log('onChange', event.target.value);
});
element.addEventListener('open', () => {
    console.log('onOpen');
});
```

## Methods

### Get/Set Value
```javascript
const element = document.getElementById('#gradient');
// set value
element.value = '{"alpha":[{"progress":0,"value":0},{"progress":1,"value":1}],"color":[{"progress":0.9174107142857143,"value":"#c93333"}]}';

// get value
const colorObject = element.value;
```

> **Note:** This is a built-in UI component for Cocos Creator Editor. It provides a gradient editor for creating and editing color and alpha gradients. 