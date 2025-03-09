# UI Label Component

## Initialize

### Basic Usage

Basic label:
```html
<ui-label>Label Text</ui-label>
```

### With Value

Label with value:
```html
<ui-label value="Label Text"></ui-label>
```

### States

Disabled label:
```html
<ui-label disabled>Disabled Label</ui-label>
```

Readonly label:
```html
<ui-label readonly>Readonly Label</ui-label>
```

Hidden label:
```html
<ui-label hidden>Hidden Label</ui-label>
```

### Text Styles

Primary label:
```html
<ui-label class="primary">Primary Label</ui-label>
```

Success label:
```html
<ui-label class="success">Success Label</ui-label>
```

Warning label:
```html
<ui-label class="warning">Warning Label</ui-label>
```

Danger label:
```html
<ui-label class="danger">Danger Label</ui-label>
```

## Parameters

### Attributes
```typescript
value = ''; // text content
disabled; // statement
readonly; // statement
hidden; // statement
```

## Events

### Available Events
```typescript
change // value changed event
```

### Usage Examples

#### Vue.js
```html
<ui-label
    @change="onChange($event.target.value)"
>Label Text</ui-label>
```

#### Vanilla JavaScript
```html
<ui-label id="label">Label Text</ui-label>
```

```javascript
const element = document.getElementById('#label');

// addEventListener
element.addEventListener('change', (event) => {
    // changed value
    console.log(event.target.value);
});
```

## Get/Set Value
```javascript
const element = document.getElementById('#label');
// set value
element.value = 'New Label Text';

// get value
const text = element.value;
```

> **Note:** This is a built-in UI component for Cocos Creator Editor. It provides a text label with various styles and states. 