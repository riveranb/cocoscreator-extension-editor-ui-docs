# UI Image Component

## Initialize

### Asset UUID Value

```html
<ui-image value="24c419ea-63a8-4ea1-a9d0-7fc469489bbc@f9941"></ui-image>
```

### Asset URL Value

```html
<ui-image value="db://internal/default_ui/atom.png/texture"></ui-image>
```

### Fill

Full of width and height:
```html
<ui-image fill value="52ef29ed-bd92-4e94-ab2f-0ebc91bf3a60" style="width: 100px; height: 50px;"></ui-image>
```

### Size

Generate image thumbnails:
```html
<ui-image droppable="cc.ImageAsset" value="52ef29ed-bd92-4e94-ab2f-0ebc91bf3a60" size="50,50"></ui-image>
```

### Droppable

Receive drag and drop, change its value:
```html
<ui-image droppable="cc.ImageAsset" size="50,50" value="52ef29ed-bd92-4e94-ab2f-0ebc91bf3a60"></ui-image>
<ui-image droppable="cc.ImageAsset,file" value="db://internal/default_ui/atom.png/texture" size="50,50"></ui-image>
```

### Position

Horizontal center, vertical middle:
```html
<ui-image value="db://internal/default_ui/atom.png/texture" style="width: 100px; height: 50px;"></ui-image>
```

### Origin Width Height

```html
<ui-image value="52ef29ed-bd92-4e94-ab2f-0ebc91bf3a60"></ui-image>
```

### Fixed Width

Auto height:
```html
<ui-image value="52ef29ed-bd92-4e94-ab2f-0ebc91bf3a60" style="width: 100px;"></ui-image>
```

### Fixed Height

Auto width:
```html
<ui-image value="52ef29ed-bd92-4e94-ab2f-0ebc91bf3a60" style="height: 80px;"></ui-image>
```

### Channel

Show the channel data of one image. The value is the combination of 'r','g','b','a'.
Usage cases: baked images in Light Map extension.

```html
<ui-image value="db://internal/default_ui/atom.png/texture"></ui-image>
<ui-image channel="r" value="db://internal/default_ui/atom.png/texture"></ui-image>
<ui-image channel="g" value="db://internal/default_ui/atom.png/texture"></ui-image>
<ui-image channel="b" value="db://internal/default_ui/atom.png/texture"></ui-image>
<ui-image channel="a" value="db://internal/default_ui/atom.png/texture"></ui-image>
<ui-image channel="rgb" value="db://internal/default_ui/atom.png/texture"></ui-image>
<ui-image channel="rgba" value="db://internal/default_ui/atom.png/texture"></ui-image>
```

### States

Readonly image:
```html
<ui-image readonly droppable="cc.ImageAsset" value="24c419ea-63a8-4ea1-a9d0-7fc469489bbc@f9941"></ui-image>
```

Disabled image:
```html
<ui-image disabled droppable="cc.ImageAsset" value="24c419ea-63a8-4ea1-a9d0-7fc469489bbc@f9941"></ui-image>
```

Invalid image:
```html
<ui-image invalid value="24c419ea-63a8-4ea1-a9d0-7fc469489bbc@f9941"></ui-image>
```

Hidden image:
```html
<ui-image hidden value="24c419ea-63a8-4ea1-a9d0-7fc469489bbc@f9941"></ui-image>
```

## Parameters

### Attributes
```typescript
value
fill
size // use its thumbnail, size="width,height", like: size="100,100"
droppable // 'cc.ImageAsset',  enable accept drop
channel // show the channel of a image, the value is the combination of 'r','g','b','a'.
readonly
disabled
```

## Events

### Available Events
```typescript
confirm
```

### Usage Examples

#### Vue.js
```html
<ui-image ref="image" droppable="cc.ImageAsset,cc.Texture2D,cc.SpriteFrame" value="24c419ea-63a8-4ea1-a9d0-7fc469489bbc@f9941"
    @confirm="confirm($event.target.value)"
></ui-image>
```

#### Vanilla JavaScript
```html
<ui-image id="image" droppable="cc.ImageAsset" value="24c419ea-63a8-4ea1-a9d0-7fc469489bbc@f9941"></ui-image>
```

```javascript
const element = document.getElementById('#image');

// addEventListener
element.addEventListener('confirm', (event) => {
    // get value
    const imageValue = event.target.value;
});
```

## Methods

### Get/Set Value
```javascript
// Vue.js
this.$refs.image.value = '24c419ea-63a8-4ea1-a9d0-7fc469489bbc@f9941';
const imageValue = this.$refs.file.value;

// Vanilla JavaScript
const element = document.getElementById('#image');
element.value = '24c419ea-63a8-4ea1-a9d0-7fc469489bbc@f9941';
const imageValue = element.value;
```

> **Note:** This is a built-in UI component for Cocos Creator Editor. It provides an image viewer and selector with support for different image formats, channels, and drag-drop functionality. 