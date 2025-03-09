# UI Slider Component

## Initialize

### Basic Usage

Basic slider:
```html
<ui-slider></ui-slider>
```

### With Value

Slider with value:
```html
<ui-slider value="50"></ui-slider>
```

### With Range

Slider with min and max:
```html
<ui-slider min="0" max="100" value="50"></ui-slider>
```

### With Step

Slider with step:
```html
<ui-slider step="10" value="50"></ui-slider>
```

### States

Disabled slider:
```html
<ui-slider disabled></ui-slider>
```

Readonly slider:
```html
<ui-slider readonly></ui-slider>
```

Invalid slider:
```html
<ui-slider invalid></ui-slider>
```

Hidden slider:
```html
<ui-slider hidden></ui-slider>
```

## Parameters

### Attributes
```typescript
value = 0; // number
min = 0; // minimum value
max = 100; // maximum value
step = 1; // step value
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
<ui-slider
    :min="0"
    :max="100"
    :step="10"
    @change="onChange($event.target.value)"
    @confirm="onConfirm($event.target.value)"
></ui-slider>
```

#### Vanilla JavaScript
```html
<ui-slider id="slider" min="0" max="100" step="10"></ui-slider>
```

```javascript
const element = document.getElementById('#slider');

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
const element = document.getElementById('#slider');
// set value
element.value = 60;

// get value
const value = element.value;
```

> **Note:** This is a built-in UI component for Cocos Creator Editor. It provides a slider control for numeric input within a specified range. 