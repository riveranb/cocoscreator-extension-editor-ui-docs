# UI Component

## Initialize

### Basic Usage with Droppable

```html
<ui-component droppable="cc.Camera"></ui-component>
```

### Value Missing Example

```html
<ui-component droppable="cc.DirectionalLight" value="xxx" missing effective></ui-component>
```

### With Placeholder

```html
<ui-component droppable="cc.Camera" placeholder="i18n:ui-kit.preview.ui.component.placeholder"></ui-component>
```

### States

Readonly component:
```html
<ui-component readonly droppable="cc.Canvas"></ui-component>
```

Disabled component:
```html
<ui-component disabled droppable="cc.Canvas"></ui-component>
```

Invalid component:
```html
<ui-component invalid></ui-component>
```

Hidden component:
```html
<ui-component hidden></ui-component>
```

## Parameters

### Attributes
```typescript
droppable = ''; // component type, not support multiple types
placeholder = '';
value = ''; // component uuid, single，not support multiple
disabled; // statement
readonly; // statement
invalid; // statement
```

## Events

### Available Events
```typescript
change // general case use this event
confirm
cancel
```

### Usage Examples

#### Vue.js
```html
<ui-component droppable="cc.Camera" ref="component"
    @change="onChange($event.target.value)"
    @confirm="onConfirm($event.target.value)"
    @cancel="onCancel($event.target.value)"
></ui-component>
```

#### Vanilla JavaScript
```html
<ui-component droppable="cc.Camera" id="component"></ui-component>
```

```javascript
const element = document.getElementById('#component');

// addEventListener
element.addEventListener('change', (event) => {
    const nodeUuid = event.target.value;
});
element.addEventListener('change', (event) => {
    console.log('onChange', event.target.value);
});
element.addEventListener('cancel', (event) => {
    console.log('onCancel', event.target.value);
});
```

## Get/Set Value
```javascript
const element = document.getElementById('#component');
// set value
element.value = componentUuid; // componentUuid already exist

// get value
const componentUuid = element.value;
```

> **Note:** This is a built-in UI component for Cocos Creator Editor. It provides a component reference field that supports drag and drop functionality. 