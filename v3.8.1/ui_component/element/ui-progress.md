# UI Progress Component

## Initialize

### Value Examples

```html
<ui-progress></ui-progress>
<ui-progress value="60"></ui-progress>
<ui-progress value="100"></ui-progress>
```

### Percent Display

```html
<ui-progress percent></ui-progress>
<ui-progress value="100" percent></ui-progress>
```

### Success State

```html
<ui-progress value="60" success></ui-progress>
```

### Failure State

```html
<ui-progress value="60" failure></ui-progress>
```

## Parameters

### Attributes
```typescript
value // progress value (0-100)
percent // whether to show percentage
success // success state styling
failure // failure state styling
```

> **Note:** This is a built-in UI component for Cocos Creator Editor. It provides a progress bar with support for percentage display and success/failure states. 