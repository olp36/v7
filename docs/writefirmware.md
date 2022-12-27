# olp36 ファームウェアの書込

olp36シリーズのファームウェアを書込む方法です。

## 目次

<!-- vim-markdown-toc GFM -->

* [Windows](#windows)
* [Mac](#mac)

<!-- vim-markdown-toc -->

## Windows

[QMK MSYS](https://msys.qmk.fm/)をインストールします。
最新リリースは、[ここ](https://github.com/qmk/qmk_distro_msys/releases/latest)から入手できます。

QMK MSYSをインストール後、QMK MSYSにて、以下のコマンドを実行します。
 `<hoge>` の部分はユーザー名に入れ替えてください。

```
qmk setup olp36/qmk_firmware --branch olp36 --home C:/Users/<hoge>/GitHub/qmk_firmware
```

全てのプロンプトに `y` と答えます。
完了したら、以下のコマンドを実行することで、正常にセットアップが完了しているかを確認することができます。

```
qmk hello
```

コンパイルの確認には、以下のコマンドを実行します。

```
qmk compile -kb olp36 -km default
```

最後に、olp36のファームウェアを接続されたキーボードに書き込みます。
QMK MSYSにて、以下のコマンドを実行します。

```
qmk flash -kb olp36 -km default
```

初回リセットは、裏面の２箇所を短絡させることで行うことができます。
書込み後のリセットは、[キーマップ](https://github.com/olp36/olp36v7/blob/main/docs/keymaps.md)をご覧ください。

![](assets/9.png)


## Mac

[Homebrew](https://brew.sh) をインストールし、ターミナルで以下のコマンドを実行し、QMK CLI をインストールします。

```
brew install qmk/qmk/qmk
```

QMK CLIをインストール後、ターミナルにて、以下のコマンドを実行します。
 `<hoge>` の部分はユーザー名に入れ替えてください。

```
qmk setup olp36/qmk_firmware --branch olp36 --home /Users/<hoge>/Documents/GitHub/qmk_firmware
```

全てのプロンプトに `y` と答えます。
完了したら、以下のコマンドを実行することで、正常にセットアップが完了しているかを確認することができます。

```
qmk hello
```

コンパイルの確認には、以下のコマンドを実行します。

```
qmk compile -kb olp36 -km mac
```

最後に、olp36のファームウェアを接続されたキーボードに書き込みます。
ターミナルにて、以下のコマンドを実行します。

```
qmk flash -kb olp36 -km mac
```

初回リセットは、裏面の２箇所を短絡させることで行うことができます。
書込み後のリセットは、[キーマップ](https://github.com/olp36/olp36v7/blob/main/docs/keymaps.md)をご覧ください。

![](assets/9.png)

