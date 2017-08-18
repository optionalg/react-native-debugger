# Getting Started

Just these steps let you start RNDebugger out of box:

* All `http://localhost:<port>/debugger-ui` pages are closed
* Make sure RNDebugger is open and wait state, or you can use [react-native-debugger-open](../npm-package) npm package instead, it can:
  * Replace `open debugger-ui with Chrome` to `open React Native Debugger` from react-native packager, saving you from closing the debugger-ui page everytime it automatically opens :)
  * Detect react-native packager port then send to the app, if you launch packager with custom `--port`, this will very useful
* Enable `Debug JS Remotely` of [developer menu](https://facebook.github.io/react-native/docs/debugging.html#accessing-the-in-app-developer-menu) on your app

## Use Redux DevTools Extension API

Use the same API as [`redux-devtools-extension`](https://github.com/zalmoxisus/redux-devtools-extension#1-with-redux) is very simple:

```js
const store = createStore(
  reducer, /* preloadedState, */
  window.__REDUX_DEVTOOLS_EXTENSION__ && window.__REDUX_DEVTOOLS_EXTENSION__()
);
```

See [`Redux DevTools Integration`](redux-devtools-integration.md) section for more information.

## Platform support

* [React Native](https://github.com/facebook/react-native) >= 0.21.0
* [React Native for macOS](https://github.com/ptmt/react-native-desktop) (formerly react-native-desktop) >= 0.8.7
* [React Native for Windows](https://github.com/ReactWindows/react-native-windows/blob/master/Libraries/Devtools/setupDevtools.windows.js) (need to remove [setupDevtools.windows.js](https://github.com/ReactWindows/react-native-windows/blob/master/Libraries/Devtools/setupDevtools.windows.js))

## Examples for use RNDebugger

* [`Redux counter`](../examples/counter-with-redux)
* [`MobX counter`](../examples/counter-with-mobx) - with [`mobx-remotedev`](https://github.com/zalmoxisus/mobx-remotedev).

The examples was bootstrapped with [`create-react-native-app`](https://github.com/react-community/create-react-native-app).

## Auto-update RNDebugger app (Supported v0.5.0 after)

Currently auto-update is only supported for macOS, for Linux / Windows will show dialog of new version available for download.

You can also click `React Native Debugger` (`RND` for Linux / Windows) -> `Check for Updates...` in application menu.
