# electron-psk-boilerplate

> Boilerplate to kickstart creating an app with [Electron](https://github.com/atom/electron) and [Polymer Starter Kit](https://github.com/PolymerElements/polymer-starter-kit)

![](https://cloud.githubusercontent.com/assets/124117/11257732/f85b91d6-8e96-11e5-8d9d-45fd65968d4b.png)

## Getting started

In your directory, run:

```
$ curl -fsSL https://github.com/ragingwind/electron-psk-boilerplate/archive/master.tar.gz | tar -xz --strip-components 2
```

You can also `git clone` or [download](https://github.com/ragingwind/electron-psk-boilerplate/archive/master.zip) this repo and get contents of the `boilerplate` folder.

Yet ~~There's also a [Yeoman generator](https://github.com/ragingwind/generator-electron).~~


## Patch for running route properly

### For v1.1.1

You should add the following code to `src/app/elements/routing.html`. See [the doc](https://github.com/PolymerElements/polymer-starter-kit/blob/master/docs/chrome-dev-editor.md) for further information.

```js
page('*', function() {
  page.redirect('/');
});
```

### For v1.2.1

You probably see the notification about route failed that could be annoyed but you could ignore it as update by code below in commenting toast code.

```js
// 404
page('*', function() {
  // app.$.toast.text = 'Can\'t find: ' + window.location.href  + '. Redirected you to Home Page';
  // app.$.toast.show();
  page.redirect(app.baseUrl);
});
```

## License

MIT © [ragingwind](http://ragingwind.me)
