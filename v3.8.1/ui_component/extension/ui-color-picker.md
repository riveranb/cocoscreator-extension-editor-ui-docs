# UI Color Picker Component

## Initialize

### Basic Usage

```html
<ui-color-picker></ui-color-picker>
```

## Parameters

### Attributes
```typescript
value
disabled
readonly
invalid
hidden
```

## Events

### Available Events
```typescript
change
confirm
```

### Usage Examples

#### Vue.js
```html
<ui-color-picker
    @change="onChange($event.target.value)"
    @confirm="onConfirm($event.target.value)"
></ui-color-picker>
```

#### Vanilla JavaScript
```html
<ui-color-picker id="ui-color-picker"></ui-color-picker>
```

```typescript
const element = document.getElementById('#ui-color-picker');

// addEventListener
element.addEventListener('change', (event) => {
    // changed value
    console.log(event.target.value)
});
element.addEventListener('confirm', (event) => {
    // confirm value
    console.log(event.target.value)
});
```

## Methods

### Get/Set Value
```typescript
const element = document.getElementById('#ui-color-picker');
// set value
element.value = 'value';

// get value
const colorValue = element.value;
```

> **Note:** This is a built-in UI component for Cocos Creator Editor. It provides a color picker interface for selecting and editing colors with support for various color formats. 