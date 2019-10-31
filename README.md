# 📦 wow.export
wow.export is a node-webkit port of [Marlamin's](https://github.com/Marlamin) [WoW Export Tools](https://github.com/Marlamin/WoWExportTools/) which provides tools for extracting and converting files from the World of Warcraft game client or public CDN servers.

## Features
- Soon™

## Installing
To install wow.export, navigate to the ['Releases'](https://github.com/Kruithne/wow.export/releases) page and download the latest version. That's it!

## Updating
When an update to wow.export is available, you will be prompted in the application to update. This process is done entirely automatically once you accept the update!

> ***OSX/Linux**: We are currently not producing builds targeted for non-Windows builds. If you wish to use wow.export on OSX or Linux, you will need to compile your own build from the source. See GH-1 for known issues.

## Building (Developers Only)
- 🔨 Building wow.export **requires** Node 12.12.0 or above.
- 🧙‍ For building on Windows, [node-gyp prerequisites](https://github.com/nodejs/node-gyp#on-windows) **may** be required.
- 🍷 For building Windows builds on platforms **other** than Windows, Wine 1.6 or above is required.

```
git fetch https://github.com/Kruithne/wow.export.git
npm install

# This will list available builds.
node ./build.js

# This will compile -all- available builds.
node ./build.js *

# Substitute <BUILD> for the build(s) you wish to compile, space-delimitated.
node ./build.js <BUILD1> <BUILD2> ...
```

## Debugging (Developers Only)
> **Note**: Debugging is currently only supported on Windows.

To debug wow.export, compile a `win-x64-debug` build using the build script. This will produce a bare-bones build using the SDK framework and without any production polish. Open starting the debug version, DevTools will be automatically launched alongside the application.

For the debug build, source code will not be compiled, rather a symlink is created. This changes to the source code are instantly reflected in the application, simply press F5 in DevTools to refresh sources.

Since stylesheets are written in Sass and no source compilation is done, you will need a transpiler for your IDE to ensure that Sass files are automatically transpiled to raw CSS during development (do not commit these).