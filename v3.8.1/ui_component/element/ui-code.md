# UI Code Component

## Initialize

### Basic Usage

HTML code example:
```html
<ui-button language="html">Show Button Code</ui-button>
```

Example usage:
```html
<ui-code language="html">
    &lt;ui-button language="html"&gt;Show Button Code&lt;/ui-button&gt;
</ui-code>
```

### TypeScript Example

```html
<ui-code language="typescript">
    export const methods = {};
    export function data() {
        return {};
    }
</ui-code>
```

### JSON Example

```html
<ui-code language="json">
[
    {
        "title": "apples",
        "count": [12000, 20000],
        "description": {"text": "...", "sensitive": false}
    }
]
</ui-code>
```

### States

Disabled code:
```html
<ui-code language="html" disabled>
    &lt;ui-button language="html"&gt;Show Button Code&lt;/ui-button&gt;
</ui-code>
```

## Parameters

### Attributes
```typescript
language // 'typescript' | 'javascript' | 'json' | 'css' | 'html' ...
disabled // Provide a style, like below
```

> **Note:** This is a built-in UI component for Cocos Creator Editor. It provides syntax-highlighted code display with support for multiple programming languages. 