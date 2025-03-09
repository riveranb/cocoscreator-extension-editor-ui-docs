# UI Tooltip Component

## Initialize

### Use in Attribute with Text

```html
<ui-label tooltip="Hello" value="I have tooltip attribute. Hover me."></ui-label>
<ui-label tooltip="i18n:ui-kit.title" value="Support i18n"></ui-label>
```

### As an Element with Custom Content

```html
<ui-tooltip>Hello</ui-tooltip>
```

### Arrow Positions

```html
<ui-tooltip arrow="top">Hello</ui-tooltip>
<ui-tooltip arrow="right">Hello</ui-tooltip>
<ui-tooltip arrow="bottom">Hello</ui-tooltip>
<ui-tooltip arrow="left">Hello</ui-tooltip>
```

### Custom Content

```html
<ui-tooltip arrow="top">
    Hello<br>
    Cocos Creator<br>
    <ui-image style="width: 64px;" value="packages://about/static/image/splash_portrait.png"></ui-image>
</ui-tooltip>
```

### Custom Arrow Position

```html
<ui-tooltip arrow="top left">...</ui-tooltip>
<ui-tooltip arrow="top center">...</ui-tooltip>
<ui-tooltip arrow="right middle">...</ui-tooltip>
<ui-tooltip arrow="bottom right">...</ui-tooltip>
```

### Animation

```html
<ui-tooltip animation>
    Hello<br>
    Cocos Creator<br>
    <ui-image style="width: 64px;" value="packages://about/static/image/splash_portrait.png"></ui-image>
</ui-tooltip>
```

### States

Disabled tooltip:
```html
<ui-tooltip disabled>Hello</ui-tooltip>
```

Hidden tooltip:
```html
<ui-tooltip hidden>Hello</ui-tooltip>
```

## Parameters

### Attributes
```typescript
arrow // 'top' | 'right' | 'bottom' | 'left' | 'top left' | 'top center' | 'right middle' | 'bottom right'
disabled
readonly
animation
hidden
```

> **Note:** This is a built-in UI component for Cocos Creator Editor. It provides a tooltip with customizable content, arrow positions, and animation support. 