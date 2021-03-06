react-panels
===========
### [Demo/examples](http://theadd.github.io/react-panels/) &nbsp; [Features](#features) &nbsp; [Playground](http://theadd.github.io/react-panels/playground/) &nbsp; [Install](#install) &nbsp; [Usage](#usage)

A multipurpose tabbed panel component with many features. Using [React](http://facebook.github.io/react/) **v0.13.1** with addons.

[![NPM](https://nodei.co/npm/react-panels.png?downloads=true&stars=true)](https://nodei.co/npm/react-panels/)


## Features

* No dependencies, single JS file with React inline styles.
  * Written to be **browser first** from the start so our browser build is a simple javascript file instead of a *webpack/browserify* bundle like in other react components. Nevertheless, this doesn't mean that *react-panels* is not suited for other kind of projects since a CommonJS build [is also provided](#install).
* Support for themes and skins.
  * Available themes: *chemical* <sup>[demo](http://theadd.github.io/react-panels/bower_components/react-panels/examples/floating/index.html)</sup>, *flexbox* <sup>[demo](http://theadd.github.io/react-panels/bower_components/react-panels/examples/flexbox/basic/index.html)</sup>, *flexbox2* <sup>*No demo yet*</sup>.
  * *Wanna share one of your own? Open an issue or make a pull request.*
* Fixed or as a draggable floating panel.
* Multi-content components and toggleable footer and toolbars in tabs.
* Auto-collapsible tab header buttons when don't fit in a single row.
* Custom panel buttons.
* Easily extensible by *mixins*. <sup>*Not documented yet*</sup>
* **Animations** <sup>[demo](http://theadd.github.io/react-panels/bower_components/react-panels/examples/flexbox/animations/index.html)</sup>
* **Drag&drop** tabs <sup>[demo](http://theadd.github.io/react-panels/bower_components/react-panels/examples/flexbox/animations-dnd/index.html)</sup> **Warning**: In development, subject to change.


## Roadmap

* Optional *className* in props to allow CSS styling.
* Restore collapsed tab headers when there's available space. <sup>*(not needed in flex based themes)*</sup>
* Allow prebuilt styles to increase performance.
* More...


## Install

**Using bower**
```sh
bower install react-panels
```
Include ```bower_components/react-panels/dist/react-panels[.min].js``` after ```react-with-addons[.min].js```

**Using npm**
```sh
npm install react-panels
```
```js
var ReactPanels = require('react-panels')
// or
var ReactPanels = require('react-panels/addons')
```


## Usage

*Example usage:*

```jsx
var Panel = ReactPanels.Panel;
var Tab = ReactPanels.Tab;
var Toolbar = ReactPanels.Toolbar;
var Content = ReactPanels.Content;
var Footer = ReactPanels.Footer;

var MyPanel = React.createClass({
  render: function () {
    return (
      <Panel theme="chemical">
        <Tab title="One" icon="fa fa-plane">
          <Toolbar>Toolbar content of One</Toolbar>
          <Content>Content of One</Content>
          <Footer>Footer content of One</Footer>
        </Tab>
        <Tab title="Two" icon="fa fa-fire">
          <Content>Content of Two</Content>
        </Tab>
      </Panel>
    );
  }
});
```

Documentation for **react-panels v2** is not available yet but you can take a look at the [working examples](http://theadd.github.io/react-panels/) for easy usages of almost all its features.


## Contributing

Feel free to fork this repo and make a **PR**. Any help is welcome, even fixing typos. I created **react-panels** to use it myself and I'm mostly adding new features or bug fixes on a need basis. So, if you need something specific, you can add/fix it yourself or open a new issue and I'll provide feedback as soon as possible.

**Thanks to**

* [yap cheah shen](https://github.com/yapcheahshen) for his [contributions](https://github.com/Theadd/react-panels/commits?author=yapcheahshen).


## Compatibility

* Compatible with [MoreartyJS](https://github.com/moreartyjs/moreartyjs). <sup>[*Slightly tweaked*](https://github.com/Theadd/react-panels/blob/c3af7999177b4f36fcb9fff5960f6684df6ab412/dist/react-panels.js#L580)</sup>
* Tested in Google Chrome, Mozilla Firefox, Opera and Internet Explorer 10 & 11.


## [License](https://github.com/Theadd/react-panels/blob/master/LICENSE)

The MIT License (MIT)
