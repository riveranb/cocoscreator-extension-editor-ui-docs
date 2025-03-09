# UI Setting Component

## Initialize

### Basic Usage

```html
<ui-setting></ui-setting>
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
<ui-setting
    @change="onChange($event.target.value)"
    @confirm="onConfirm($event.target.value)"
></ui-setting>
```

#### Vanilla JavaScript
```html
<ui-setting id="ui-setting"></ui-setting>
```

```typescript
const element = document.getElementById('#ui-setting');

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
const element = document.getElementById('#ui-setting');
// set value
element.value = 'value';

// get value
const settingValue = element.value;
```

> **Note:** This is a built-in UI component for Cocos Creator Editor. It provides a settings interface for configuring various options and preferences. 