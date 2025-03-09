# UI Checkbox Component

## Initialize

### Basic Usage

Basic checkbox:
```html
<ui-checkbox></ui-checkbox>
```

### With Value

Checked checkbox:
```html
<ui-checkbox value="true"></ui-checkbox>
```

Unchecked checkbox:
```html
<ui-checkbox value="false"></ui-checkbox>
```

### States

Disabled checkbox:
```html
<ui-checkbox disabled></ui-checkbox>
```

Readonly checkbox:
```html
<ui-checkbox readonly></ui-checkbox>
```

Invalid checkbox:
```html
<ui-checkbox invalid></ui-checkbox>
```

Hidden checkbox:
```html
<ui-checkbox hidden></ui-checkbox>
```

## Parameters

### Attributes
```typescript
value = false; // boolean
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
<ui-checkbox
    @change="onChange($event.target.value)"
    @confirm="onConfirm($event.target.value)"
></ui-checkbox>
```

#### Vanilla JavaScript
```html
<ui-checkbox id="checkbox"></ui-checkbox>
```

```javascript
const element = document.getElementById('#checkbox');

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
const element = document.getElementById('#checkbox');
// set value
element.value = true;

// get value
const checked = element.value;
```

> **Note:** This is a built-in UI component for Cocos Creator Editor. It provides a customizable checkbox element with various states and events. 