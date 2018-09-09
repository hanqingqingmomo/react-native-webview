# React Native WebView - a Modern, Cross-Platform WebView for React Native

**React Native WebView** is a modern, well-supported, and cross-platform WebView for React Native. It is intended to be a replacement for the built-in WebView (which will be [removed from core](https://github.com/react-native-community/discussions-and-proposals/pull/3)).

**Please note that this package is pre-release and not yet ready for production use.**

## Platforms Supported

* [x] iOS (both UIWebView and WKWebView)
* [x] Android
* [ ] Windows 10 (coming soon)

## Installation

*Note: this is currently a work-in-progress and not yet published to NPM.*

```
$ npm install --save https://github.com/react-native-community/react-native-webview
$ react-native link react-native-webview
```

## Usage

Import the `WebView` component from `react-native-webview` and use it like so:

```jsx
import React, { Component } from 'react'
import { StyleSheet, Text, View } from 'react-native'
import { WebView } from 'react-native-webview'

// ...
class MyWebComponent extends Component {
  render () {
    return (
      <WebView
        src={{uri: "https://infinite.red/react-native"}}
        style={{marginTop: 20}}
      />
    )
  }
}
```

Additional properties are supported and will be added here; for now, refer to the previous React Native WebView documentation for more.

[https://facebook.github.io/react-native/docs/webview](https://facebook.github.io/react-native/docs/webview)

## Migrate from React Native core WebView to React Native WebView

Simply install React Native WebView and then use it in place of the core WebView. Their APIs are currently identical, except that this package defaults `useWebKit={true}` unlike the built-in WebView.

### Contributor Notes

* I've removed all PropTypes for now. Instead, we'll be moving toward Flow or TypeScript at a later date
* UIWebView is not tested fully and you will encounter some yellow warning boxes. Since it is deprecated, we don't intend to put a lot of time into supporting it, but feel free to submit PRs if you have a special use case. Note that you will need to specify `useWebKit={false}` to use UIWebView

## Maintainers

* [Jamon Holmgren](https://github.com/jamonholmgren) ([Twitter](https://twitter.com/jamonholmgren)) from [Infinite Red](https://infinite.red/react-native)

## License

MIT
