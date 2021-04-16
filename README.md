react-custom-scrollbars-2
=========================

[![npm](https://img.shields.io/badge/npm-react--custom--scrollbars--2-brightgreen.svg?style=flat-square)]()
[![npm version](https://img.shields.io/npm/v/react-custom-scrollbars-2.svg?style=flat-square)](https://www.npmjs.com/package/react-custom-scrollbars-2)
[![npm downloads](https://img.shields.io/npm/dm/react-custom-scrollbars-2.svg?style=flat-square)](https://www.npmjs.com/package/react-custom-scrollbars-2)

* frictionless native browser scrolling
* native scrollbars for mobile devices
* [fully customizable](https://github.com/RobPethick/react-custom-scrollbars-2/blob/master/docs/customization.md)
* [auto hide](https://github.com/RobPethick/react-custom-scrollbars-2/blob/master/docs/usage.md#auto-hide)
* [auto height](https://github.com/RobPethick/react-custom-scrollbars-2/blob/master/docs/usage.md#auto-height)
* [universal](https://github.com/RobPethick/react-custom-scrollbars-2/blob/master/docs/usage.md#universal-rendering) (runs on client & server)
* `requestAnimationFrame` for 60fps
* no extra stylesheets
* well tested, 100% code coverage

**[Demos](https://robpethick.github.io/react-custom-scrollbars-2/) · [Documentation](https://github.com/RobPethick/react-custom-scrollbars-2/tree/master/docs)**

## Quick note
This repo is due to the original (fantastic) [`react-custom-scrollbars`](https://www.npmjs.com/package/react-custom-scrollbars) package going a little stale and we needed a handful of bug fixes which will be managed here.

## Installation
```bash
npm install react-custom-scrollbars-2 --save
```

This assumes that you’re using [npm](http://npmjs.com/) package manager with a module bundler like [Webpack](http://webpack.github.io) or [Browserify](http://browserify.org/) to consume [CommonJS modules](http://webpack.github.io/docs/commonjs.html).

If you don’t yet use [npm](http://npmjs.com/) or a modern module bundler, and would rather prefer a single-file [UMD](https://github.com/umdjs/umd) build that makes `ReactCustomScrollbars` available as a global object, you can grab a pre-built version from [unpkg](https://unpkg.com/react-custom-scrollbars-2@4.3.0/dist/react-custom-scrollbars.js). We *don’t* recommend this approach for any serious application, as most of the libraries complementary to `react-custom-scrollbars-2` are only available on [npm](http://npmjs.com/).

## Usage

This is the minimal configuration. [Check out the Documentation for advanced usage](https://github.com/RobPethick/react-custom-scrollbars-2/tree/master/docs).

```javascript
import { Scrollbars } from 'react-custom-scrollbars-2';

class App extends Component {
  render() {
    return (
      <Scrollbars style={{ width: 500, height: 300 }}>
        <p>Some great content...</p>
      </Scrollbars>
    );
  }
}
```

The `<Scrollbars>` component is completely customizable. Check out the following code:

```javascript
import { Scrollbars } from 'react-custom-scrollbars-2';

class CustomScrollbars extends Component {
  render() {
    return (
      <Scrollbars
        onScroll={this.handleScroll}
        onScrollFrame={this.handleScrollFrame}
        onScrollStart={this.handleScrollStart}
        onScrollStop={this.handleScrollStop}
        onUpdate={this.handleUpdate}
        renderView={this.renderView}
        renderTrackHorizontal={this.renderTrackHorizontal}
        renderTrackVertical={this.renderTrackVertical}
        renderThumbHorizontal={this.renderThumbHorizontal}
        renderThumbVertical={this.renderThumbVertical}
        autoHide
        autoHideTimeout={1000}
        autoHideDuration={200}
        autoHeight
        autoHeightMin={0}
        autoHeightMax={200}
        thumbMinSize={30}
        universal={true}
        {...this.props}>
    );
  }
}
```

All properties are documented in the [API docs](https://github.com/RobPethick/react-custom-scrollbars-2/blob/master/docs/API.md)

## Examples

Run the simple example:
```bash
# Make sure that you've installed the dependencies
npm install
# Move to example directory
cd react-custom-scrollbars-2/examples/simple
npm install
npm start
```

## Tests
```bash
# Make sure that you've installed the dependencies
npm install
# Run tests
npm test
```

### Code Coverage
```bash
# Run code coverage. Results can be found in `./coverage`
npm run test:cov
```


## License

MIT
