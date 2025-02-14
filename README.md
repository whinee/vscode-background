# vscode-background

[![Version](https://vsmarketplacebadge.apphb.com/version/shalldie.background.svg?style=flat-square&logo=visual-studio-code)](https://marketplace.visualstudio.com/items?itemName=shalldie.background)
[![Installs](https://vsmarketplacebadge.apphb.com/installs/shalldie.background.svg?style=flat-square)](https://marketplace.visualstudio.com/items?itemName=shalldie.background)
[![Ratings](https://vsmarketplacebadge.apphb.com/rating/shalldie.background.svg?style=flat-square)](https://vsmarketplacebadge.apphb.com/rating/shalldie.background.svg)
[![Build Status](https://img.shields.io/github/workflow/status/shalldie/vscode-background/ci?label=build&logo=github&style=flat-square)](https://github.com/shalldie/vscode-background/actions)

[English](./README.md) | [中文](./README.zh-CN.md)

[GitHub](https://github.com/shalldie/vscode-background) | [Vscode Market](https://marketplace.visualstudio.com/items?itemName=shalldie.background)

---

Bring background images to your [Visual Studio Code](https://code.visualstudio.com)

![](https://user-images.githubusercontent.com/9987486/40583705-7105dda8-61c6-11e8-935a-3c5d475a1eb1.gif)

## Installation

To install the extension just execute the following command in the Command Palette of Visual Studio Code

```
ext install background
```

## Custom

User defined requirements can be met by changing the configuration(`settings.json`).

[what's settings.json](https://code.visualstudio.com/docs/getstarted/settings#_settingsjson) | [where is](https://github.com/shalldie/vscode-background/issues/274)

## Config

| Name                      |      Type       |   Default    | Description                                 |
| :------------------------ | :-------------: | :----------: | :------------------------------------------ |
| `background.enabled`      |    `Boolean`    |    `true`    | Enable or disable this plugin               |
| `background.useFront`     |    `Boolean`    |    `true`    | Set the image to front or back of your code |
| `background.useDefault`   |    `Boolean`    |    `true`    | Whether or not to use default images        |
| `background.style`        |    `Object`     |     `{}`     | Customize style                             |
| `background.styles`       | `Array<Object>` | `[{},{},{}]` | Add custom Style for individual image       |
| `background.customImages` | `Array<String>` |     `[]`     | Add your custom images                      |
| `background.loop`         |    `Boolean`    |   `false`    | `loop` mode, may repeat your images         |

`style` means [css style](https://developer.mozilla.org/en-US/docs/Learn/CSS/First_steps/What_is_CSS), which allows you to create great-looking background.

## Examples

1. disable this extension

```json
{
  "background.enabled": false
}
```

2. custom images

You should use protocol **https** instead of **http** for the image, **http** is not support by vscode any more.

```json
{
  "background.useDefault": false,
  "background.customImages": ["https://a.com/b.png", "file:///Users/somepath/a.jpg"]
}
```

3. custom style - opacity

```json
{
  "background.style": {
    "opacity": 0.6
  }
}
```

4. custom style - image size

```json
{
  "background.style": {
    "background-size": "300px 460px"
  }
}
```

5. custom style - full screen

[Related Issue](https://github.com/shalldie/vscode-background/issues/268)

```json
{
  "background.style": {
    "background-size": "cover",
    "position": "fixed"
  }
}
```

## Warns

> **This extension works by editting the vscode's css file.**
>
> So, a warning appears while the first time to install or vscode update. U can click the [never show again] to avoid it.

![](https://user-images.githubusercontent.com/9987486/40583926-b1fb5398-61ca-11e8-8271-4ac650d158d3.png)

This is the reason:

![](https://user-images.githubusercontent.com/9987486/40583775-91d4c8d6-61c7-11e8-9048-8c5538a32399.png)

## Uninstall

    two ways

    1. (recommended)

    press `F1` to open Command Palette, enter and chose `Background - Uninstall (remove extension)` , automatically complete uninstall.

    2.

    Set the config  {"background.enabled": false}  in settings.json, then uninstall the plugin.

## Contributors 🙏

[<img alt="shalldie" src="https://avatars3.githubusercontent.com/u/9987486?v=4" width="80">](https://github.com/shalldie)
[<img alt="NoDocCat" src="https://avatars.githubusercontent.com/u/20502666?v=4" width="80">](https://github.com/NoDocCat)
[<img alt="frg2089" src="https://avatars.githubusercontent.com/u/42184238?v=4" width="80">](https://github.com/frg2089)
[<img alt="mwSora" src="https://avatars.githubusercontent.com/u/23083011?v=4" width="80">](https://github.com/mwSora)
[<img alt="tumit" src="https://avatars.githubusercontent.com/u/1756190?v=4" width="80">](https://github.com/tumit)
[<img alt="asurinsaka" src="https://avatars.githubusercontent.com/u/8145535?v=4" width="80">](https://github.com/asurinsaka)
[<img alt="u3u" src="https://avatars.githubusercontent.com/u/20062482?v=4" width="80">](https://github.com/u3u)
[<img alt="kuresaru" src="https://avatars.githubusercontent.com/u/31172177?v=4" width="80">](https://github.com/kuresaru)
[<img alt="Unthrottled" src="https://avatars.githubusercontent.com/u/15972415?v=4" width="80">](https://github.com/Unthrottled)
[<img alt="rogeraabbccdd" src="https://avatars.githubusercontent.com/u/15815422?v=4" width="80">](https://github.com/rogeraabbccdd)

## CHANGELOG

You can checkout all our changes in our [change log](https://github.com/shalldie/vscode-background/blob/master/CHANGELOG.md).

## Q&A

---

    Q: How to remove [unsupported] tag?
    A: see here: https://github.com/lehni/vscode-fix-checksums

---

    Q: It seems that nothing happens after installing the extension in MAC?
    A: In Mac, move `vscode` from `Download` to `Applications`.

---

    Q: The extension runs based on the modified vscode CSS file, and will try to raise the right within a limited time.
       If it stop working for some reason, what if users need to change their permissions?

    A: In windows,click right button on the vscode's icon,then check the [run with the administrator authority].
    A: in mac/linux, try this: https://github.com/shalldie/vscode-background/issues/6 .

---

## LICENSE

MIT
