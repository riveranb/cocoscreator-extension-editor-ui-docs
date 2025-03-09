# Dialog Component

## Initialize

### Message Dialogs

```html
<ui-button @click="show('info')">info</ui-button>
<ui-button @click="show('warn')">warn</ui-button>
<ui-button @click="show('error')">error</ui-button>
```

```typescript
async show(type: string) {
    const config: any = {
        title: type,
        detail: 'detail',
    };
    const code = await Editor.Dialog[type](`${type} + message`, config);
    console.log(code);
}
```

### Custom Buttons

```html
<ui-button @click="buttons()">buttons</ui-button>
```

```typescript
async buttons() {
    const config: any = {
        title: 'buttons',
        detail: 'detail',
        buttons: ['a', 'b', 'c', 'd'],
    };
    const code = await Editor.Dialog.info('info + message', config);
    console.log(code);
}
```

### File Selection

#### Open File Dialog

```html
<ui-button @click="openFile()">default</ui-button>
<ui-button @click="openFile('root')">Designated folder</ui-button>
<ui-button @click="openFile('filters')">filters</ui-button>
```

```typescript
async openFile(type: string) {
    const config: any = {};

    switch (type) {
        case 'root':
            config.path = __dirname;
            break;
        case 'filters':
            config.filters = [
                { name: 'Images', extensions: ['jpg', 'png', 'gif'] },
            ];
            break;
    }

    const data = await Editor.Dialog.select(config);
    console.log(data);
}
```

#### Open Directory Dialog

```html
<ui-button @click="openDirectory()">default</ui-button>
```

```typescript
async openDirectory() {
    const config: any = {
        type: 'directory',
    };
    const data = await Editor.Dialog.select(config);
    console.log(data);
}
```

### Save Dialog

```html
<ui-button @click="save()">default</ui-button>
<ui-button @click="save('root')">Designated folder</ui-button>
```

```typescript
async save(type: string) {
    const config: any = {};

    switch (type) {
        case 'root':
            config.path = __dirname;
            break;
    }

    const data = await Editor.Dialog.save(config);
    console.log(data);
}
```

## Methods

### Message Dialogs
```typescript
Editor.Dialog.info(message: string, options?: DialogOptions): Promise<number>
Editor.Dialog.warn(message: string, options?: DialogOptions): Promise<number>
Editor.Dialog.error(message: string, options?: DialogOptions): Promise<number>
```

### File Dialogs
```typescript
Editor.Dialog.select(options: SelectDialogOptions): Promise<string[]>
Editor.Dialog.save(options: SaveDialogOptions): Promise<string>
```

## Types

### DialogOptions
```typescript
interface DialogOptions {
    title?: string;
    detail?: string;
    buttons?: string[];
}
```

### SelectDialogOptions
```typescript
interface SelectDialogOptions {
    path?: string;
    type?: 'directory' | 'file';
    filters?: Array<{
        name: string;
        extensions: string[];
    }>;
}
```

### SaveDialogOptions
```typescript
interface SaveDialogOptions {
    path?: string;
}
```

> **Note:** This is a built-in dialog system for Cocos Creator Editor. It provides various types of dialogs including message dialogs (info, warning, error), file selection dialogs, and save dialogs with customizable options. 