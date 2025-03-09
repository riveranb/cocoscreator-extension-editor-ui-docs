# UI Number Input Component

## Initialize

### Basic Usage with Value

Can drag to change value:
```html
<ui-num-input value="666"></ui-num-input>
```

### Step

If not set step, default step will be used by preference:
```html
<ui-num-input value="10" step="1"></ui-num-input>
```

### Precision (preci)

Correct decimal places number:
```html
<ui-num-input value="10" preci="0"></ui-num-input>
<ui-num-input value="10.123" preci="2"></ui-num-input>
<ui-num-input value="10.153" preci="1"></ui-num-input>
```

### Min/Max

```html
<ui-num-input value="9" step="1" min="5"></ui-num-input>
<ui-num-input value="9" step="1" max="10"></ui-num-input>
<ui-num-input value="9" step="1" min="5" max="10"></ui-num-input>
<ui-num-input value="90" step="1" min="5" max="10"></ui-num-input>
```

### Unit

```html
<ui-num-input value="10" unit="px"></ui-num-input>
```

### Label

```html
<ui-num-input label="X" value="0"></ui-num-input>
```

### States

Invalid number input:
```html
<ui-num-input invalid></ui-num-input>
```

Readonly number input:
```html
<ui-num-input readonly value="0"></ui-num-input>
```

Disabled number input:
```html
<ui-num-input disabled value="0"></ui-num-input>
```

Hidden number input:
```html
<ui-num-input hidden value="0"></ui-num-input>
```

## Parameters

### Attributes
```typescript
value
unit
label
preci
step
max
min
disabled
readonly
invalid
placeholder
hidden
```

## Events

### Available Events
```typescript
change // general case use this event
confirm
cancel
unit-click
```

### Usage Examples

#### Vue.js
```html
<ui-num-input unit="px"
    @change="onChange($event.target.value)"
    @confirm="onConfirm($event.target.value)"
    @cancel="onCancel($event.target.value)"
    @unit-click="onUnitClick"
></ui-num-input>
```

#### Vanilla JavaScript
```html
<ui-num-input id="ui-num-input" unit="px"></ui-num-input>
```

```javascript
const element = document.getElementById('#ui-num-input');

// addEventListener
element.addEventListener('change', (event) => {
    // changed value
    console.log('onChange', event.target.value)
});
element.addEventListener('confirm', (event) => {
    // confirm value
    console.log('onConfirm', event.target.value)
});
element.addEventListener('cancel', (event) => {
    // cancel value
    console.log('onCancel', event.target.value)
});
element.addEventListener('unit-click', () => {
    console.log('unit-click')
});
```

> **Note:** This is a built-in UI component for Cocos Creator Editor. It provides a numeric input field with support for step values, precision, min/max constraints, units, and labels. 