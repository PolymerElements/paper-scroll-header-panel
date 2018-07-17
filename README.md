[![Published on NPM](https://img.shields.io/npm/v/@polymer/paper-scroll-header-panel.svg)](https://www.npmjs.com/package/@polymer/paper-scroll-header-panel)
[![Build status](https://travis-ci.org/PolymerElements/paper-scroll-header-panel.svg?branch=master)](https://travis-ci.org/PolymerElements/paper-scroll-header-panel)
[![Published on webcomponents.org](https://img.shields.io/badge/webcomponents.org-published-blue.svg)](https://webcomponents.org/element/@polymer/paper-scroll-header-panel)

## &lt;paper-scroll-header-panel&gt;

**This element has been deprecated in favor of [app-layout](https://github.com/PolymerElements/app-layout).**

`paper-scroll-header-panel` contains a header section and a content section.  The
header is initially on the top part of the view but it scrolls away with the
rest of the scrollable content.  Upon scrolling slightly up at any point, the
header scrolls back into view.  This saves screen space and allows users to
access important controls by easily moving them back to the view.

__Important:__ The `paper-scroll-header-panel` will not display if its parent does not have a height.

`paper-scroll-header-panel` works well with `paper-toolbar` but can use any element
that represents a header by adding a `paper-header` class to it.

Note: If the class `paper-header` is used, the header must be positioned relative or absolute. e.g.

```css
.paper-header {
  position: relative;
}
```

```html
<paper-scroll-header-panel>
  <div class="paper-header" slot="header">Header</div>
  <div slot="content">Content goes here...</div>
</paper-scroll-header-panel>
```

### Styling

=======

The following custom properties and mixins are available for styling:

| Custom property | Description | Default |
| --- | --- | --- |
| --paper-scroll-header-panel-full-header | To change background for toolbar when it is at its full size | {} |
| --paper-scroll-header-panel-condensed-header | To change the background for toolbar when it is condensed | {} |
| --paper-scroll-header-panel-container | To override or add container styles | {} |
| --paper-scroll-header-panel-header-container | To override or add header styles | {} |

See: [Documentation](https://www.webcomponents.org/element/@polymer/paper-scroll-header-panel),
  [Demo](https://www.webcomponents.org/element/@polymer/paper-scroll-header-panel/demo/demo/index.html).

## Usage

### Installation
```
npm install --save @polymer/paper-scroll-header-panel
```

### In an html file
```html
<html>
  <head>
    <script type="module">
      import '@polymer/paper-scroll-header-panel/paper-scroll-header-panel.js';
      import '@polymer/paper-toolbar/paper-toolbar.js';
    </script>
    <style>
      html, body {
        margin: 0;
      }
      paper-scroll-header-panel {
        height: 100vh;
      }
    </style>
  </head>
  <body>
    <paper-scroll-header-panel>
      <paper-toolbar slot="header">
        <div>Hello World!</div>
      </paper-toolbar>
      <div slot="content">Content goes here...</div>
    </paper-scroll-header-panel>
  </body>
</html>
```
### In a Polymer 3 element
```js
import {PolymerElement, html} from '@polymer/polymer';
import '@polymer/paper-scroll-header-panel/paper-scroll-header-panel.js';
import '@polymer/paper-toolbar/paper-toolbar.js';

class SampleElement extends PolymerElement {
  static get template() {
    return html`
      <style>
        paper-scroll-header-panel {
          height: 100vh;
        }
      </style>
      <paper-scroll-header-panel>
        <paper-toolbar slot="header">
          <div>Hello World!</div>
        </paper-toolbar>
        <div slot="content">Content goes here...</div>
      </paper-scroll-header-panel>
    `;
  }
}
customElements.define('sample-element', SampleElement);
```

## Contributing
If you want to send a PR to this element, here are
the instructions for running the tests and demo locally:

### Installation
```sh
git clone https://github.com/PolymerElements/paper-scroll-header-panel
cd paper-scroll-header-panel
npm install
npm install -g polymer-cli
```

### Running the demo locally
```sh
polymer serve --npm
open http://127.0.0.1:<port>/demo/
```

### Running the tests
```sh
polymer test --npm
```
