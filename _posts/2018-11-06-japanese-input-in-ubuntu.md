---
layout: post
title: ubuntuで日本語入力設定
---

# 日本語入力設定

* OS: Ubuntu 18.04
* 言語: 英語

##  Mozc インストール

* Mozcがデフォルトで入っていないためインストール

```shell
$ sudo apt  install ibus-mozc
```

* Mozcを入力方式に追加:
  * Settings > Regions and Language > Input Sources > Add (+ ボタン)
  * Start barからMozc追加されたことを確認

## Mozc変換をCtrl Spaceキーに設定

* Mozc設定でKeymapをCustomize -> Edit -> New Entry
* IMEの有効と無効を以下の通りに設定

| Mode | Key | Command |
| --- | --- | --- |
| Driect Input | Ctrl Space | Actice IME |
| Compositon | Ctrl Space | Deactive IME |
| Precompostion | Ctrl Space | Deactive IME |
| Conversion | Ctrl Space | Deactive IME |

* 即反映されるが、駄目だったらログオフしてみると行ける場合がある
