paper-scroll-header-panel
========================

`paper-scroll-header-panel` contains a header section and a content section. The header is initially on the top part of the view but it scrolls away with the rest of the scrollable content. Upon scrolling slightly up at any point, the header scrolls back into view. This saves screen space and allows users to access important controls by easily moving them back to the view.

Important: The `paper-scroll-header-panel` will not display if its parent does not have a height. Using layout classes, you can easily make the `paper-scroll-header-panel` fill the screen

```html
<body class="fullbleed layout vertical">
  <paper-scroll-header-panel class="flex">
    <paper-toolbar>
      Hello World!
    </paper-toolbar>
  </paper-scroll-header-panel>
</body>
```
or, if you would prefer to do it in CSS, just give html, body, and `paper-scroll-header-panel` a height of 100%:
```css
html, body {
  height: 100%;
  margin: 0;
}
paper-scroll-header-panel {
  height: 100%;
}
```
`paper-scroll-header-panel` works well with `paper-toolbar` but can use any element that represents a header by adding a `paper-header` class to it.

```html
<paper-scroll-header-panel>
  <paper-toolbar>
    App Tile
  </paper-toolbar>
  <div>
    Content goes here...
  </div>
</paper-scroll-header-panel>
```

You can enable the condensed mode and define a `transformable` element. In this mode,
the header's height will condense to `condensedHeaderHeight` as the user scrolls 
down from the top of the content area.

```html
<paper-scroll-header-panel condenses>
  <paper-toolbar>
    <div class="title transformable">
      App Name
    </div>
  </paper-toolbar>
  <div>
    Content goes here...
  </div>
</paper-scroll-header-panel>
```

### Styling scroll-header-panel:

To change background for toolbar when it is at its full size:

```css
paper-scroll-header-panel {
  --paper-scroll-header-panel-full-header: {
    background-color: red;
  };
}
```

To change the background for toolbar when it is condensed:

```css
paper-scroll-header-panel {
  --paper-scroll-header-panel-condensed-header: {
    background-color: #f4b400;
  };
}
```
