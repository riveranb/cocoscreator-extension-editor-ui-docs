# UI Tab Component

## Initialize

### Default Style
```html
<ui-tab>
    <ui-button active>Web</ui-button>
    <ui-button>IOS</ui-button>
    <ui-button>Android</ui-button>
    <ui-button>Mini Game</ui-button>
</ui-tab>
```

### Set Active Tab by Value
The number is the index of the button (0-based):
```html
<ui-tab value="2">
    <ui-button>Web</ui-button>
    <ui-button>IOS</ui-button>
    <ui-button active>Android</ui-button>
    <ui-button>Mini Game</ui-button>
</ui-tab>
```

### Underline Style
```html
<ui-tab underline>
    <ui-button active>Web</ui-button>
    <ui-button>IOS</ui-button>
    <ui-button>Android</ui-button>
    <ui-button>Mini Game</ui-button>
</ui-tab>
```

### Disabled State
```html
<ui-tab disabled>
    <ui-button disabled active>Web</ui-button>
    <ui-button disabled>IOS</ui-button>
    <ui-button disabled>Android</ui-button>
    <ui-button disabled>Mini Game</ui-button>
</ui-tab>

<ui-tab disabled underline>
    <ui-button disabled active>Web</ui-button>
    <ui-button disabled>IOS</ui-button>
    <ui-button disabled>Android</ui-button>
    <ui-button disabled>Mini Game</ui-button>
</ui-tab>
```

### Width Overflow
```html
<ui-tab style="width: 100px;">
    <ui-button active>Web</ui-button>
    <ui-button>IOS</ui-button>
    <ui-button>Android</ui-button>
    <ui-button>Mini Game</ui-button>
</ui-tab>

<ui-tab underline style="width: 100px;">
    <ui-button active>Web</ui-button>
    <ui-button>IOS</ui-button>
    <ui-button>Android</ui-button>
    <ui-button>Mini Game</ui-button>
</ui-tab>
```

## Parameters

### Attributes
```typescript
value // index of active tab
disabled
underline // enable underline style
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
<ui-tab value="0"
    @change="onChange($event.target.value)"
    @confirm="onConfirm($event.target.value)"
>
    <ui-button>Web</ui-button>
    <ui-button>IOS</ui-button>
    <ui-button>Android</ui-button>
    <ui-button>Mini Game</ui-button>
</ui-tab>
```

#### Vanilla JavaScript
```html
<ui-tab id="ui-tab" value="0">
    <ui-button>Web</ui-button>
    <ui-button>IOS</ui-button>
    <ui-button>Android</ui-button>
    <ui-button>Mini Game</ui-button>
</ui-tab>
```

```typescript
const element = document.getElementById('#ui-tab');

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
const element = document.getElementById('#ui-tab');
// set value
element.value = '0';

// get value
const tabValue = element.value;
```

> **Note:** This is a built-in UI component for Cocos Creator Editor. It provides a tab interface for organizing content into multiple selectable views with support for different styles and states. 