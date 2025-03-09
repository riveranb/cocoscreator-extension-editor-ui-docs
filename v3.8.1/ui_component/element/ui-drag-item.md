# UI Drag Item Component

## Initialize

### Basic Usage

```html
<ui-drag-item></ui-drag-item>
```

### With Value

```html
<ui-drag-item value="item1"></ui-drag-item>
```

### With Type

```html
<ui-drag-item type="cc.Node"></ui-drag-item>
```

### States

Disabled drag item:
```html
<ui-drag-item disabled></ui-drag-item>
```

Readonly drag item:
```html
<ui-drag-item readonly></ui-drag-item>
```

Invalid drag item:
```html
<ui-drag-item invalid></ui-drag-item>
```

Hidden drag item:
```html
<ui-drag-item hidden></ui-drag-item>
```

## Parameters

### Attributes
```typescript
value // drag item value
type // drag item type, like: 'cc.Node'
disabled
readonly
invalid
hidden
```

## Events

### Available Events
```typescript
dragstart // when drag starts
dragend // when drag ends
```

### Usage Examples

#### Vue.js
```html
<ui-drag-item ref="dragItem"
    value="item1"
    type="cc.Node"
    @dragstart="onDragStart"
    @dragend="onDragEnd"
></ui-drag-item>
```

#### Vanilla JavaScript
```html
<ui-drag-item id="dragItem" value="item1" type="cc.Node"></ui-drag-item>
```

```javascript
const element = document.getElementById('#dragItem');

// addEventListener
element.addEventListener('dragstart', (event) => {
    console.log('onDragStart');
});
element.addEventListener('dragend', (event) => {
    console.log('onDragEnd');
});
```

> **Note:** This is a built-in UI component for Cocos Creator Editor. It provides a draggable item that can be used in conjunction with ui-drag-area for drag and drop functionality. 