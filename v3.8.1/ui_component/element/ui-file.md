# UI File Component

## Initialize

### Basic Usage

```html
<ui-file></ui-file>
```

### With Value

```html
<ui-file value="/Applications/Cocos/Creator/3.8.1/CocosCreator.app/Contents/Resources/app.asar"></ui-file>
```

### Type Examples

```html
<ui-file type="directory"></ui-file>
<ui-file type="file"></ui-file>
<ui-file type="app"></ui-file>
```

### Protocols

Project protocol:
```html
<ui-file type="directory" protocols="project"></ui-file>
```

Multiple protocols:
```html
<ui-file type="directory" protocols="file,project"></ui-file>
```

### With Project Path

```html
<ui-file type="directory" protocols="project" value="project://assets/test"></ui-file>
```

### With Placeholder

```html
<ui-file type="app" placeholder="Select an application"></ui-file>
```

### Multiple Selection

```html
<ui-file multi></ui-file>
```

### File Extensions

```html
<ui-file extensions="js,ts,txt"></ui-file>
```

### States

Readonly file:
```html
<ui-file readonly></ui-file>
```

Disabled file:
```html
<ui-file disabled></ui-file>
```

Invalid file:
```html
<ui-file invalid></ui-file>
```

Hidden file:
```html
<ui-file hidden></ui-file>
```

## Parameters

### Attributes
```typescript
value = '' // system file path, you can set default value
extensions = '' // filter files by extensions, using ',' join multiple ones
type = "directory" | "file" | "app"
multi // support multiple files selected
disabled
readonly
invalid
protocols // support protocols types, like: 'project'
placeholder
hidden
```

## Events

### Available Events
```typescript
change // general case use this event
confirm
```

### Usage Examples

#### Vue.js
```html
<ui-file ref="file"
    value="/Applications/Cocos/Creator/3.8.1/CocosCreator.app/Contents/Resources/app.asar"
    @confirm="confirm($event.target.value)"
    @change="onChange($event.target.value)"
></ui-file>
```

#### Vanilla JavaScript
```html
<ui-file id="file" value="/Applications/Cocos/Creator/3.8.1/CocosCreator.app/Contents/Resources/app.asar"></ui-file>
```

```javascript
const element = document.getElementById('#file');

// addEventListener
element.addEventListener('confirm', (event) => {
    // get value
    console.log('onConfirm', event.target.value);
});
element.addEventListener('change', (event) => {
    // get value
    const filepath = event.target.value;
});
```

## Methods

### Get/Set Value
```javascript
const element = document.getElementById('#file');
// set value
element.value = '/Applications/Cocos/Creator/3.8.1/CocosCreator.app/Contents/Resources/app.asar';

// get value
const filepath = element.value;
```

### Editor.UI.File.resolveToRaw
Resolve project path to raw path:
```javascript
const element = document.getElementById('#file');
if (element.value.startsWith('project://')) {
    const path = Editor.UI.File.resolveToRaw(element.value);
    console.log(`raw path: ${path}`);
}
```

### Editor.UI.File.resolveToUrl
Resolve raw path to project path:
```javascript
const element = document.getElementById('#file');
if (!element.value.startsWith('project://')) {
    // first param must be raw file path
    const path = Editor.UI.File.resolveToUrl(element.value, 'project');
    console.log(`project path: ${path}`);
}
```

### Editor.UI.File.getAllProtocolInfos
```javascript
const protocolInfos = Editor.UI.File.getAllProtocolInfos();
console.log(protocolInfos[0].protocol);
```

> **Note:** This is a built-in UI component for Cocos Creator Editor. It provides a file selector with support for different file types, protocols, and multiple selection. 