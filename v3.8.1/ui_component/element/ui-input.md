# UI Input Component

## Initialize

### Basic Usage

Basic input:
```html
<ui-input></ui-input>
```

### With Value

Input with value:
```html
<ui-input value="input value"></ui-input>
```

### With Placeholder

Input with placeholder:
```html
<ui-input placeholder="Please input..."></ui-input>
```

### States

Disabled input:
```html
<ui-input disabled></ui-input>
```

Readonly input:
```html
<ui-input readonly></ui-input>
```

Invalid input:
```html
<ui-input invalid></ui-input>
```

Hidden input:
```html
<ui-input hidden></ui-input>
```

### Input Types

Password input:
```html
<ui-input type="password"></ui-input>
```

Number input:
```html
<ui-input type="number"></ui-input>
```

### Size

Small input:
```html
<ui-input class="small"></ui-input>
```

Large input:
```html
<ui-input class="large"></ui-input>
```

## Parameters

### Attributes
```typescript
value = ''; // string
placeholder = '';
type = 'text'; // text | password | number
disabled; // statement
readonly; // statement
invalid; // statement
hidden; // statement
```

## Events

### Available Events
```typescript
change // general case use this event
confirm // press enter key
cancel // press esc key
```

### Usage Examples

#### Vue.js
```html
<ui-input
    @change="onChange($event.target.value)"
    @confirm="onConfirm($event.target.value)"
    @cancel="onCancel"
></ui-input>
```

#### Vanilla JavaScript
```html
<ui-input id="input"></ui-input>
```

```javascript
const element = document.getElementById('#input');

// addEventListener
element.addEventListener('change', (event) => {
    // changed value
    console.log(event.target.value);
});
element.addEventListener('confirm', (event) => {
    // confirm value
    console.log(event.target.value);
});
element.addEventListener('cancel', () => {
    console.log('onCancel');
});
```

## Get/Set Value
```javascript
const element = document.getElementById('#input');
// set value
element.value = 'new value';

// get value
const value = element.value;
```

> **Note:** This is a built-in UI component for Cocos Creator Editor. It provides a customizable input field with various states and events. 