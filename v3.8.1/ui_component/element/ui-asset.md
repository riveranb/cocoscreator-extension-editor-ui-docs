# UI Asset Component

## Initialize

### Droppable

Drop Image Asset here:
```html
<ui-asset droppable="cc.ImageAsset"></ui-asset>
```

### Multiple Types

Drop Animation or Image Asset here:
```html
<ui-asset droppable="cc.AnimationClip, cc.ImageAsset"></ui-asset>
```

### Placeholder

Select an asset...:
```html
<ui-asset droppable="cc.ImageAsset" placeholder="Select an asset..."></ui-asset>
```

### Value

UUID format:
```html
<ui-asset droppable="cc.ImageAsset" value="03721795-84b1-4dcd-8eb3-c8e6b88ee535"></ui-asset>
```

URL format:
```html
<ui-asset droppable="cc.ImageAsset" value="db://internal/default_cubemap/back.jpg"></ui-asset>
```

### States

Invalid:
```html
<ui-asset invalid droppable="cc.ImageAsset"></ui-asset>
```

Readonly:
```html
<ui-asset readonly droppable="cc.ImageAsset"></ui-asset>
```

Disabled:
```html
<ui-asset disabled droppable="cc.ImageAsset"></ui-asset>
```

## Parameters

### Attributes
```typescript
droppable = ''; // asset type, using ',' join multiple types
placeholder = '';
value = ''; // asset uuid, single，not support multiple
disabled; // statement
readonly; // statement
invalid; // statement
```

## Events

### Available Events
```typescript
change // general case use this event
confirm
preview
```

### Usage Examples

#### Vue.js
```html
<ui-asset droppable="cc.ImageAsset" ref="image" value="03721795-84b1-4dcd-8eb3-c8e6b88ee535"
    @change="onChange($event.target.value)"
    @confirm="onConfirm($event.target.value)"
    @preview="onPreview"
></ui-asset>
```

#### Vanilla JavaScript
```html
<ui-asset droppable="cc.ImageAsset" id="asset" value="03721795-84b1-4dcd-8eb3-c8e6b88ee535"></ui-asset>
```

```javascript
const element = document.getElementById('#asset');

// addEventListener
element.addEventListener('confirm', (event) => {
    // confirm value
    const assetUuid = event.target.value;
});
element.addEventListener('change', (event) => {
    // change value
    const assetUuid = event.target.value;
});
element.addEventListener('preview', (event) => {
    console.log('onPreview');
});
```

## Get/Set Value
```javascript
const element = document.getElementById('#asset');
// set value
element.value = '03721795-84b1-4dcd-8eb3-c8e6b88ee535';

// get value
const assetUuid = element.value;
```

> **Note:** This is a built-in UI component for Cocos Creator Editor. It can only be used within editor extensions and is specifically designed for handling asset references in the editor. 