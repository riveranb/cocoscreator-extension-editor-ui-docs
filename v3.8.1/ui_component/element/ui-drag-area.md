# UI Drag Area Component

## Initialize

### Basic Usage

```html
<ui-drag-area></ui-drag-area>
```

### With Accept Types

```html
<ui-drag-area accept="cc.Node,cc.Prefab"></ui-drag-area>
```

### With Placeholder

```html
<ui-drag-area placeholder="Drag and drop files here"></ui-drag-area>
```

### States

Disabled drag area:
```html
<ui-drag-area disabled></ui-drag-area>
```

Readonly drag area:
```html
<ui-drag-area readonly></ui-drag-area>
```

Invalid drag area:
```html
<ui-drag-area invalid></ui-drag-area>
```

Hidden drag area:
```html
<ui-drag-area hidden></ui-drag-area>
```

## Parameters

### Attributes
```typescript
accept // accept types, like: 'cc.Node,cc.Prefab'
placeholder // placeholder text
disabled
readonly
invalid
hidden
```

## Events

### Available Events
```typescript
dragenter // when drag enters the area
dragleave // when drag leaves the area
dragover // when drag is over the area
drop // when files are dropped
```

### Usage Examples

#### Vue.js
```html
<ui-drag-area ref="dragArea"
    accept="cc.Node,cc.Prefab"
    placeholder="Drag and drop files or nodes here"
    @dragenter="onDragEnter"
    @dragleave="onDragLeave"
    @dragover="onDragOver"
    @drop="onDrop"
></ui-drag-area>
```

#### Vanilla JavaScript
```html
<ui-drag-area id="dragArea" accept="cc.Node,cc.Prefab" placeholder="Drag and drop files or nodes here"></ui-drag-area>
```

```javascript
const element = document.getElementById('#dragArea');

// addEventListener
element.addEventListener('dragenter', (event) => {
    console.log('onDragEnter');
});
element.addEventListener('dragleave', (event) => {
    console.log('onDragLeave');
});
element.addEventListener('dragover', (event) => {
    console.log('onDragOver');
});
element.addEventListener('drop', (event) => {
    const files = Array.from(event.dataTransfer.files);
    console.log('onDrop', files);
});
```

> **Note:** This is a built-in UI component for Cocos Creator Editor. It provides a drag and drop area for files and nodes with customizable accept types and placeholder text. 