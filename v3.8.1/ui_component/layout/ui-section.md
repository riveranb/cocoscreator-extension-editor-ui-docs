# UI Section Component

## Initialize

### Default Style

Content with padding-left 28px:
```html
<ui-section header="Content padding-left is 28px" expand>
    <div>one</div>
    <div>two</div>
    <div>three</div>
</ui-section>
```

Using header slot:
```html
<ui-section>
    <div slot="header">slot="header"</div>
    <div>This is content</div>
</ui-section>
```

### Config Style

Header with background and no left padding:
```html
<ui-section class="config" header="Header has background, content padding-left is 0px">
    <div>This is content</div>
</ui-section>
```

### Expand

Expandable section:
```html
<ui-section header="Header text" expand>
    <div>one</div>
    <div>two</div>
    <div>three</div>
</ui-section>
```

### Whole (Non-collapsible)

Section that cannot be collapsed:
```html
<ui-section header="Can not collapse, content padding-left is 8px" whole>
    <div>one</div>
    <div>two</div>
    <div>three</div>
</ui-section>
```

Config style with whole attribute:
```html
<ui-section class="config" whole>
    <div slot="header">Can not collapse</div>
    <div>one</div>
    <div>two</div>
    <div>three</div>
</ui-section>
```

### States

Disabled section:
```html
<ui-section expand disabled>
    <div slot="header">header</div>
    <div>one</div>
    <div>two</div>
    <div>three</div>
</ui-section>
```

Readonly section:
```html
<ui-section expand readonly>
    <div slot="header">header</div>
    <div>one</div>
    <div>two</div>
    <div>three</div>
</ui-section>
```

## Parameters

### Attributes
```typescript
header
expand // initial show with expand state
whole // can not collapse
disabled
readonly
```

## Events

### Usage Examples

#### Vue.js
```html
<ui-section header="Header text"
    @expand="onExpand"
    @uiscroll="onUIscroll"
>
    <div>one</div>
    <div>two</div>
    <div>three</div>
</ui-section>
```

#### Vanilla JavaScript
```html
<ui-section id="ui-section" header="Header text">
    <div>one</div>
    <div>two</div>
    <div>three</div>
</ui-section>
```

```javascript
const element = document.getElementById('#ui-section');

// addEventListener
element.addEventListener('expand', () => {
    console.log('onExpand');
});
element.addEventListener('uiscroll', () => {
    console.log('onUIScroll');
});
```

> **Note:** This is a built-in UI component for Cocos Creator Editor. It provides a collapsible section with header and content areas. 