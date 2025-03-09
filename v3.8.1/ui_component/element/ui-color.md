# UI Color Component

## Initialize

### Basic Usage

Basic color picker:
```html
<ui-color></ui-color>
```

### With Value

Color picker with value:
```html
<ui-color value="rgb(255, 0, 0)"></ui-color>
```

### With Alpha

Color picker with alpha channel:
```html
<ui-color value="rgba(255, 0, 0, 0.5)"></ui-color>
```

### States

Disabled color picker:
```html
<ui-color disabled></ui-color>
```

Readonly color picker:
```html
<ui-color readonly></ui-color>
```

Invalid color picker:
```html
<ui-color invalid></ui-color>
```

Hidden color picker:
```html
<ui-color hidden></ui-color>
```

## Parameters

### Attributes
```typescript
value = ''; // color string (hex, rgb, rgba)
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
<ui-color
    @change="onChange($event.target.value)"
    @confirm="onConfirm($event.target.value)"
></ui-color>
```

#### Vanilla JavaScript
```html
<ui-color id="color"></ui-color>
```

```javascript
const element = document.getElementById('#color');

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
const element = document.getElementById('#color');
// set value
element.value = 'rgb(255, 0, 0)';

// get value
const color = element.value;
```

> **Note:** This is a built-in UI component for Cocos Creator Editor. It provides a color picker with support for RGB and RGBA color formats. 