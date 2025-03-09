# UI Prop Component

## Initialize

### Basic Usage

Various form elements:
```html
<ui-prop>
    <ui-label slot="label">Checkbox</ui-label>
    <ui-checkbox slot="content"></ui-checkbox>
</ui-prop>

<ui-prop>
    <ui-label slot="label">Name</ui-label>
    <ui-input slot="content"></ui-input>
</ui-prop>

<ui-prop>
    <ui-label slot="label">Color</ui-label>
    <ui-color slot="content"></ui-color>
</ui-prop>

<ui-prop>
    <ui-label slot="label">Select</ui-label>
    <ui-select slot="content">
        <option value="1">Lorem ipsum dolor sit amet consectetur, adipisicing elit. Sit, sint.</option>
        <option value="2">Sapiente ratione esse voluptatibus repudiandae illo numquam quas nulla id.</option>
    </ui-select>
</ui-prop>
```

### Readonly

```html
<ui-prop readonly>
    <ui-label slot="label">Name</ui-label>
    <ui-input slot="content"></ui-input>
</ui-prop>
```

### No Label

```html
<ui-prop no-label>
    <ui-label slot="label">Name</ui-label>
    <ui-input slot="content"></ui-input>
</ui-prop>
```

### Message

Default message:
```html
<ui-prop message="default message...">
    <ui-label slot="label">Name A</ui-label>
    <ui-input slot="content" value="name a"></ui-input>
</ui-prop>
```

Custom message with link:
```html
<ui-prop>
    <ui-label slot="label">Name B</ui-label>
    <ui-input slot="content" value="name b"></ui-input>
    <div slot="message">
        Here is a showcase with a link:
        <ui-link value="https://www.cocos.com/docs">Custom Message</ui-link>
    </div>
</ui-prop>
```

### Text Styles

Primary style:
```html
<ui-prop message="primary message..." class="primary">
    <ui-label slot="label">Name A</ui-label>
    <ui-input slot="content" value="primary"></ui-input>
</ui-prop>
```

Success style:
```html
<ui-prop message="success message..." class="success">
    <ui-label slot="label">Name B</ui-label>
    <ui-input slot="content" value="success"></ui-input>
</ui-prop>
```

Warning style:
```html
<ui-prop message="warn message..." class="warn">
    <ui-label slot="label">Name C</ui-label>
    <ui-input slot="content" value="warn"></ui-input>
</ui-prop>
```

Danger style:
```html
<ui-prop message="error message..." class="danger">
    <ui-label slot="label">Name D</ui-label>
    <ui-input slot="content" value="danger"></ui-input>
</ui-prop>
```

## Parameters

### Attributes
```typescript
readonly // just show lock icon
no-label // do not show label
message // display message below the prop
hidden
```

> **Note:** This is a built-in UI component for Cocos Creator Editor. It provides a property field with label and content areas, commonly used for form layouts. 