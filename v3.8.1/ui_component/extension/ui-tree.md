# UI Tree Component

## Initialize

### Basic Usage
```html
<ui-tree ref="example" style="height: 200px;"></ui-tree>
```

### Tree Data Structure
```typescript
interface TreeNode {
    detail: {
        value: string;
        checked: boolean;
        checkbox?: boolean;
        disabled?: boolean;
    };
    showArrow?: boolean;
    children: TreeNode[];
    index?: number;
}
```

### Complete Example
```typescript
export function mounted() {
    // @ts-ignore
    const vm = this;

    var t = {
        detail: {
            value: 'test',
            checked: false,
        },
        children: [
            {
                detail: {
                    value: 'test-2',
                    checked: false,
                },
                children: [
                    {
                        detail: {
                            value: 'test-3',
                            checked: false,
                        },
                        showArrow: false,
                        children: [],
                    },
                ],
            },
        ],
    };

    var test = [];

    for (let i = 0; i < 1000; i++) {
        test.push(JSON.parse(JSON.stringify(t)));
    }

    // Set up left template (checkbox)
    vm.$refs.example.setTemplate('left', '<ui-checkbox></ui-checkbox>');
    vm.$refs.example.setTemplateInit('left', ($left) => {
        $left.$checkbox = $left.querySelector('ui-checkbox');
        $left.$checkbox.addEventListener('confirm', (event) => {
            $left.data.detail.checkbox = !$left.data.detail.checkbox;
            vm.$refs.example.render(true);
        });
    });
    vm.$refs.example.setRender('left', ($left, data) => {
        $left.$checkbox.value = data.detail.checkbox;
    });

    // Set up text template
    vm.$refs.example.setTemplate('text', `<span class="name"></span><span class="link"></span>`);
    vm.$refs.example.setTemplateInit('text', ($text) => {
        $text.$name = $text.querySelector('.name');
        $text.$link = $text.querySelector('.link');
    });
    vm.$refs.example.setRender('text', ($text, data) => {
        $text.$name.innerHTML = data.detail.value;
        $text.$link.innerHTML = `link(${data.index})`;
    });

    // Set up right template (refresh icon)
    vm.$refs.example.setTemplate('right', '<ui-icon value="reset"></ui-icon>');
    vm.$refs.example.setTemplateInit('right', ($right) => {
        $right.$refresh = $right.querySelector('ui-icon');
        $right.$refresh.addEventListener('click', (event) => {
            console.log($right.data);
        });
    });

    // Set tree data
    vm.$refs.example.tree = test;

    // Set up keyboard navigation
    vm.$refs.example.addEventListener('keydown', (event) => {
        const $dom = vm.$refs.example;
        if (event.code === 'ArrowUp') {
            const item = $dom.selectItems[$dom.selectItems.length - 1];
            const index = Math.max(item.index - 1, 0);
            if (event.shiftKey) {
                $dom.select($dom.list[index]);
            } else {
                $dom.clear();
                $dom.select($dom.list[index]);
            }
            $dom.render();
        } else if (event.code === 'ArrowDown') {
            const item = $dom.selectItems[$dom.selectItems.length - 1];
            const index = Math.min(item.index + 1, $dom.list.length - 1);
            if (event.shiftKey) {
                $dom.select($dom.list[index]);
            } else {
                $dom.clear();
                $dom.select($dom.list[index]);
            }
            $dom.render();
        }
    });

    // Set up item template
    vm.$refs.example.setTemplateInit('item', ($div) => {
        const $dom = vm.$refs.example;
        $div.addEventListener('click', (event) => {
            if (event.ctrlKey || event.metaKey) {
                $dom.select($div.data);
            } else {
                $dom.clear();
                $dom.select($div.data);
            }
            $dom.render();
        });
    });
    vm.$refs.example.setRender('item', ($div, data) => {
        if (data.detail.disabled) {
            $div.setAttribute('disabled', '');
        } else {
            $div.removeAttribute('disabled');
        }
    });

    // Set custom CSS
    vm.$refs.example.css = `
        .item[disabled] {
            opacity: 0.4;
        }
        
        .text > .link {
            margin-left: 10px;
            cursor: pointer;
            color: yellow;
        }
        
        .right > ui-icon {
            cursor: pointer;
            color: green;
        }
    `;
}
```

## Parameters

### Attributes
```typescript
tree // tree data structure
line-height // height of each tree item
indent // indentation for child items
disabled
readonly
hidden
```

### Methods
```typescript
setTemplate(position: string, template: string) // Set template for a position (left, text, right)
setTemplateInit(position: string, callback: Function) // Initialize template
setRender(position: string, callback: Function) // Set render function for template
select(item: TreeNode) // Select a tree item
clear() // Clear selection
render(force?: boolean) // Render the tree
```

> **Note:** This is a built-in UI component for Cocos Creator Editor. It provides a highly customizable tree view with support for checkboxes, custom templates, keyboard navigation, and selection management. 