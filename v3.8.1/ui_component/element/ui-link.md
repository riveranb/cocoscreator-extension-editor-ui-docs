# UI Link Component

## Initialize

### Basic Usage

Basic link:
```html
<ui-link>Link Text</ui-link>
```

### With Value

Link with URL:
```html
<ui-link value="https://www.cocos.com">Cocos Website</ui-link>
```

### With Target

Link with target:
```html
<ui-link value="https://www.cocos.com" target="_blank">Open in New Tab</ui-link>
```

### States

Disabled link:
```html
<ui-link disabled>Disabled Link</ui-link>
```

Hidden link:
```html
<ui-link hidden>Hidden Link</ui-link>
```

### Link Styles

Primary link:
```html
<ui-link class="primary">Primary Link</ui-link>
```

Success link:
```html
<ui-link class="success">Success Link</ui-link>
```

Warning link:
```html
<ui-link class="warning">Warning Link</ui-link>
```

Danger link:
```html
<ui-link class="danger">Danger Link</ui-link>
```

## Parameters

### Attributes
```typescript
value = ''; // URL
target = '_self'; // _self | _blank | _parent | _top
disabled; // statement
hidden; // statement
```

## Events

### Available Events
```typescript
confirm // click event
```

### Usage Examples

#### Vue.js
```html
<ui-link
    value="https://www.cocos.com"
    @confirm="onClick"
>Cocos Website</ui-link>
```

#### Vanilla JavaScript
```html
<ui-link id="link" value="https://www.cocos.com">Cocos Website</ui-link>
```

```javascript
const element = document.getElementById('#link');

// addEventListener
element.addEventListener('confirm', () => {
    console.log('onClick');
});
```

## Get/Set Value
```javascript
const element = document.getElementById('#link');
// set value
element.value = 'https://www.cocos.com/new';

// get value
const url = element.value;
```

> **Note:** This is a built-in UI component for Cocos Creator Editor. It provides a hyperlink with various styles and states. 