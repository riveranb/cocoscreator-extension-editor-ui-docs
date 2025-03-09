# UI Textarea Component

## Initialize

### Basic Usage

```html
<ui-textarea value="test"></ui-textarea>
```

### Placeholder

```html
<ui-textarea placeholder="content"></ui-textarea>
<ui-textarea placeholder="i18n:ui-kit.preview.ui.textarea.placeholder"></ui-textarea>
```

### States

Invalid textarea:
```html
<ui-textarea invalid></ui-textarea>
```

Readonly textarea:
```html
<ui-textarea readonly value="test content"></ui-textarea>
```

Disabled textarea:
```html
<ui-textarea disabled value="test content"></ui-textarea>
```

### Auto Height

Automatic height increase or decrease according to the content height:
```html
<ui-textarea autoheight></ui-textarea>
```

Hidden textarea:
```html
<ui-textarea hidden></ui-textarea>
```

## Parameters

### Attributes
```typescript
value
autoheight
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
cancel // ESC cancel, restore the last value
```

### Usage Examples

#### Vue.js
```html
<ui-textarea placeholder="content"
    @change="onChange($event.target.value)"
    @confirm="onConfirm($event.target.value)"
    @cancel="onCancel($event.target.value)"
></ui-textarea>
```

#### Vanilla JavaScript
```html
<ui-textarea id="ui-textarea"></ui-textarea>
```

```javascript
const element = document.getElementById('#ui-textarea');

// addEventListener
element.addEventListener('change', (event) => {
    // changed value
    console.log(event.target.value)
});
element.addEventListener('confirm', (event) => {
    // confirm value
    console.log(event.target.value)
});
element.addEventListener('cancel', (event) => {
    // cancel value
    console.log(event.target.value)
});
```

> **Note:** This is a built-in UI component for Cocos Creator Editor. It provides a multi-line text input field with support for auto-height adjustment and various states. 