# UI Markdown Component

## Initialize

### Basic Usage

Basic markdown:
```html
<ui-markdown>
# Heading 1
## Heading 2

- List item 1
- List item 2

**Bold text** and *italic text*
</ui-markdown>
```

### With Value

Markdown with value:
```html
<ui-markdown value="# Markdown Content"></ui-markdown>
```

### States

Disabled markdown:
```html
<ui-markdown disabled># Disabled Content</ui-markdown>
```

Readonly markdown:
```html
<ui-markdown readonly># Readonly Content</ui-markdown>
```

Hidden markdown:
```html
<ui-markdown hidden># Hidden Content</ui-markdown>
```

## Parameters

### Attributes
```typescript
value = ''; // markdown content
disabled; // statement
readonly; // statement
hidden; // statement
```

## Events

### Available Events
```typescript
change // content changed event
```

### Usage Examples

#### Vue.js
```html
<ui-markdown
    @change="onChange($event.target.value)"
># Vue.js Example</ui-markdown>
```

#### Vanilla JavaScript
```html
<ui-markdown id="markdown"># JavaScript Example</ui-markdown>
```

```javascript
const element = document.getElementById('#markdown');

// addEventListener
element.addEventListener('change', (event) => {
    // changed value
    console.log(event.target.value);
});
```

## Get/Set Value
```javascript
const element = document.getElementById('#markdown');
// set value
element.value = '# New Content';

// get value
const content = element.value;
```

> **Note:** This is a built-in UI component for Cocos Creator Editor. It provides a markdown renderer with editing capabilities. 