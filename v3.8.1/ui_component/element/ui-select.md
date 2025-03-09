# UI Select Component

## Initialize

### Basic Usage

Basic select:
```html
<ui-select>
    <option value="1">Option 1</option>
    <option value="2">Option 2</option>
    <option value="3">Option 3</option>
</ui-select>
```

### With Value

Select with value:
```html
<ui-select value="2">
    <option value="1">Option 1</option>
    <option value="2">Option 2</option>
    <option value="3">Option 3</option>
</ui-select>
```

### With Placeholder

Select with placeholder:
```html
<ui-select placeholder="Please select...">
    <option value="1">Option 1</option>
    <option value="2">Option 2</option>
    <option value="3">Option 3</option>
</ui-select>
```

### States

Disabled select:
```html
<ui-select disabled>
    <option value="1">Option 1</option>
    <option value="2">Option 2</option>
    <option value="3">Option 3</option>
</ui-select>
```

Readonly select:
```html
<ui-select readonly>
    <option value="1">Option 1</option>
    <option value="2">Option 2</option>
    <option value="3">Option 3</option>
</ui-select>
```

Invalid select:
```html
<ui-select invalid>
    <option value="1">Option 1</option>
    <option value="2">Option 2</option>
    <option value="3">Option 3</option>
</ui-select>
```

Hidden select:
```html
<ui-select hidden>
    <option value="1">Option 1</option>
    <option value="2">Option 2</option>
    <option value="3">Option 3</option>
</ui-select>
```

## Parameters

### Attributes
```typescript
value = ''; // selected value
placeholder = '';
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
<ui-select
    @change="onChange($event.target.value)"
    @confirm="onConfirm($event.target.value)"
>
    <option value="1">Option 1</option>
    <option value="2">Option 2</option>
    <option value="3">Option 3</option>
</ui-select>
```

#### Vanilla JavaScript
```html
<ui-select id="select">
    <option value="1">Option 1</option>
    <option value="2">Option 2</option>
    <option value="3">Option 3</option>
</ui-select>
```

```javascript
const element = document.getElementById('#select');

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
const element = document.getElementById('#select');
// set value
element.value = '2';

// get value
const value = element.value;
```

> **Note:** This is a built-in UI component for Cocos Creator Editor. It provides a customizable select dropdown with various states and events. 