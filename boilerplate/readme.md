# appName

> desciption


## Dev

```
// latest light version of psk will be download after npm install
$ npm install
```

### Patch for running route properly

Until v1.1.1, You should add the following code to `src/app/elements/routing.html`. See [the doc](https://github.com/PolymerElements/polymer-starter-kit/blob/master/docs/chrome-dev-editor.md) for further information.

```
page('*', function() {
  page.redirect('/');
});
```

### Run

```
$ npm start
```

### Build

```
$ npm run build
```

Builds the app for OS X, Linux, and Windows, using [electron-packager](https://github.com/maxogden/electron-packager).

## License

MIT © [username](website)
