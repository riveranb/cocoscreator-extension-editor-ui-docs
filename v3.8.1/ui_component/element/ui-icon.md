# UI Icon Component

## Initialize

### Basic Usage

```html
<ui-icon value="component"></ui-icon>
```

### With Default Value

When the value is not found, the default value is used:
```html
<ui-icon default="component" value="cc.Label"></ui-icon>
```

### Hidden State

```html
<ui-icon hidden></ui-icon>
```

## Icon Categories

### Asset Icons
- animation-graph
- animation-graph-variant
- animation
- animation-clip
- animation-mask
- audio-clip
- auto-atlas
- bin

### Component Icons
- box
- button
- billboard
- camera
- canvas
- capsule
- component
- cone
- cylinder
- directional-light
- event
- label
- layout
- light
- node
- node-2d
- node-3d
- particle
- plane
- progress-bar
- quad
- sphere
- sphere-comp
- scrollview
- slider
- scrollbar
- spot-light
- sphere-light
- sprite-splash
- transform
- toggle
- torus
- widget
- webview

### Object Icons
- bell
- code
- font
- file
- folder
- folder-open
- home
- help
- info
- info-i
- line
- log
- menu
- music
- qr-code
- question
- radar
- ref-map
- star

### Operation Icons
- switch-open
- switch-close
- add
- add-more
- arrange
- align-bottom
- align-h-center
- align-left
- align-more-down
- align-more-up
- align-right
- align-top
- align-v-center
- clear
- copy
- close
- check
- collapse
- collapse-right
- checkbox
- checkbox-some
- checkbox-checked
- curve
- check-b
- close-b
- close-o
- clear-o
- del
- distribute-bottom
- distribute-h-center
- distribute-left
- distribute-right
- distribute-top
- distribute-v-center
- drag-asset
- drag-component
- drag-node
- edit
- error
- exit
- expand
- export
- examine
- experiment
- eye-close
- eye-open
- eye-close-b
- eye-open-b
- filter
- forward
- fullscreen
- import
- location
- list
- link
- lock
- next-play
- next-step
- no-drop
- maxi
- mini
- pause
- pin
- play
- prev-play
- popup
- radio
- radio-checked
- reset
- refresh
- rewind
- reduce
- readonly
- rotate
- save
- stop
- scale-origin
- select
- success
- setting
- sort-more
- search
- search-more
- save-o
- search-b
- unpin
- unlink
- unlock
- un-maxi
- warn
- warn-triangle
- zoomin
- zoomout

### Package Icons
- assets
- assets-preview
- animator
- builder
- code-editor
- dev-tools
- extension
- hierarchy
- inspector
- service
- picture
- shortcuts
- build-bundle

### Platform Icons
- android
- computer
- html5
- ios
- mini-game
- mobile
- wechat

## Parameters

### Attributes
```typescript
value // icon name from the available categories
default // fallback icon when value is not found
hidden // hide the icon
```

> **Note:** This is a built-in UI component for Cocos Creator Editor. It provides a comprehensive set of icons organized by categories for use throughout the editor interface. 