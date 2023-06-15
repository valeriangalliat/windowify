# 🏞️ Windowify

> Open a picture as a macOS window.

## Installation

```
git clone https://github.com/valeriangalliat/windowify.git
```

Then either put that folder in your `PATH` or use as `./windowify`.

## Usage

```
windowify [options] [<attribute>...] <file>
```

**Arguments:**

* `<file>` Path to an image.
* `<attribute>` Attribute name, prefixed with `+` or `-` to enable or
  disable it.

**Options:**

* `-h`, `--help` Show help.
* `--title <title>` Set title.
* `--minimal` Shortcut for `-closable -miniaturizable -resizable
  +fullSizeContentView +titlebarAppearsTransparent +titleHidden`.

**Attributes:**

| Attribute                    | Default |
|------------------------------|---------|
| `titled`                     | `true`  |
| `closable`                   | `true`  |
| `miniaturizable`             | `true`  |
| `resizable`                  | `true`  |
| `fullSizeContentView`        | `false` |
| `titlebarAppearsTransparent` | `false` |
| `titleHidden`                | `false` |
| `closeButtonHidden`          | `false` |
| `miniaturizeButtonHidden`    | `false` |
| `zoomButtonHidden`           | `false` |

You can press <kbd>Command</kbd> + <kbd>W</kbd> to quit.

## Example

Using this picture as example:

![Example](example.jpg)

```sh
windowify example.jpg
```

![Screenshot of window showing the image with a title bar and usual buttons](../../raw/screenshots/default.png)

```sh
windowify +fullSizeContentView +titlebarAppearsTransparent example.jpg
```

![Screenshot of window showing the image with a floating title bar](../../raw/screenshots/floating.png)

```sh
windowify --minimal example.jpg
```

![Screenshot of window showing the image with no title bar](../../raw/screenshots/minimal.png)

## Why?

The reason I initially developed that was to fake a screenshot of a
macOS dialog with the native transparent shadow. See
[blog post](https://www.codejam.info/2023/04/macos-screenshot-dialog.html)
for details!
