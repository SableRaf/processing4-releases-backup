# [Processing 4.2](https://github.com/benfry/processing4/releases/tag/processing-1292-4.2)

_Revision 1292 – 20 February 2023_

Impress your friends with new `pde://` protocol handlers! With Processing 4.2, you can link to `.pdex` and `.pdez` files to immediately run and install libraries and sketches. How it works:

- Linking to `pde://processing.org/somesketch.pdez` in the browser will download `somesketch.pdez` and load it into the editor. It also works for files, for instance `pde:///Users/ada/Desktop/somesketch.pdez` will open an archive found on the Desktop.
- This also works for contributions (Libraries, Modes, Tools) archived as `.pdex` files.

Both file types are simply a renamed `.zip` file. So to create sketches in `.pdez` format, use Tools → Archive Sketch, and replace the `.zip` with `.pdez`.

This is implemented for macOS and Windows ([#559](https://github.com/processing/processing4/issues/559)), based on [this article](https://web.archive.org/web/20210601082308/https://support.shotgunsoftware.com/hc/en-us/articles/219031308-How-to-launch-external-applications-using-custom-protocols-rock-instead-of-http-?mobile_site=true) which appears to be from [@pboucher](https://github.com/pboucher). Thank you! We still need help with implementing and testing it on Linux ([#674](https://github.com/processing/processing4/issues/674)). We would also like to add a warning dialog when opening files this way ([#560](https://github.com/processing/processing4/issues/560)).

In addition to the protocol handlers, there are a number of fixes in this release, especially for Windows users (and soon, for Python users).

## Windows users, we still love you

- The `.pde`, `.pdex`, and `.pdez` icons now work on Windows!
- Exporting projects to Windows resulted in “cannot find Java” errors, now fixed. [#667](https://github.com/processing/processing4/issues/667)

## Snake people, we love you too

- Several internal changes have been made to better support future releases of [Python Mode](https://github.com/jdf/processing.py/tree/processing4). Fingers crossed that we'll be able to launch some of this soon.

## And still we fix the bugs

- Fix encoding problem in “has been resized from 100?100 to 116?100 by the window manager” messages when using OpenGL.
- `fullScreen(P2D)` not using the full screen when Windows display is scaled to fractional sizes. [#514](https://github.com/processing/processing4/issues/514).
- `Table.getString()` raises stack overflow when column type set to `double`. [#671](https://github.com/processing/processing4/issues/671)
- Added support chained decimals during SVG Parsing (contribution from [@bsapozhnikov](https://github.com/bsapozhnikov)) [#515](https://github.com/processing/processing4/issues/515), [#659](https://github.com/processing/processing4/pull/659)
- Applications were being exported to the wrong folder. [#601](https://github.com/processing/processing4/issues/601)
- Fixed more `/tmp` folder problems on Linux. [#666](https://github.com/processing/processing4/issues/666)
