# フロントコース環境構築

フロントコースを受講するために必要な環境構築を行なっていきます。  

## GitHubの改行コード設定（Windowsの方）

Macの方は改行コードの設定は不要になるのでツールのインストールに進んでください。

改行コードについて少しだけ説明すると、Macは改行コードがLF、WindowsはCRLFになっています。  
GitHub上では改行コードがLFで管理されているため、Windowsの方がGitHubからソースコードを取得すると改行コードが自動的にCRLFに変換されてしまいます。

すると、「改行コードはLFを使ってください」というエラーが発生してしまうため、改行コードをLFのまま取得するように設定を変更していきます。

ターミナルを開いて下記のコマンドを実行してください。

```sh
git config --global core.autocrlf input
```

次に下記のコマンドを実行し`core.autocrlf=input`という記述が表示されれば問題ありません。

```sh
git config --global --list
```

## ツールのインストール

下記をインストールしていきます。

- Homebrew(Macの方のみ)

### Homebrew
※Windowsの方はHomebrewの設定は飛ばして、Voltaの設定に進んでください。  
HomebrewとはMacのためのパッケージ管理システムです。  
パッケージ管理システムとは、パッケージを一元管理し、管理を自動化するシステムのことを指します。

具体的にはHomebrewを使用することで、パッケージのインストールやアンインストール、バージョンの切り替えを簡単に行えるようになります。  
それでは、Homebrewをインストールしていきましょう。

ターミナルを開いて下記のコマンドを実行してください。

```shell
/bin/bash -c "$(curl -fsSL https://raw.githubusercontent.com/Homebrew/install/HEAD/install.sh)"
```

しばらく待ってインストールが完了したら、下記のコマンドを実行しHomebrewがインストールされているか確認しましょう。

```shell
brew -v
```

下記のようにHomebrewのバージョンが表示されれば、Homebrewのインストールは完了です。

```shell
Homebrew 3.5.9
Homebrew/homebrew-core (git revision d1409ew; last commit 2022-08-22)
```

#### 「zsh: command not found: brew」が表示される場合
こちらのメッセージが表示された方は、追加で設定が必要なので下記コマンドを実行してください。  
※下記コマンドの「ユーザー名」の部分には自分のPCのユーザー名を入れてください。

```shell
echo 'eval "$(/opt/homebrew/bin/brew shellenv)"' >> /Users/ユーザー名/.zprofile
eval "$(/opt/homebrew/bin/brew shellenv)"
```

再度`brew -v`を実行してバージョンが表示されれば、Homebrewのインストールは完了です。

```shell
brew -v

Homebrew 3.5.9
Homebrew/homebrew-core (git revision d1409ew; last commit 2022-08-22)
```