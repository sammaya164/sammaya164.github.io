---
title: "#04_JekyllのMinimal Mistakesテーマをインストールする"
categories: "ラズパイ"
---

## Jekyllとは
* ホームページ作成ツールの一種
* データベースやCGIを必要としない(静的)
* Rubyで書かれている
* Markdown記法が使える
* プログラムコードのシンタックスハイライトが使える

### 参考
Jekyllの公式サイト  
[https://jekyllrb.com/](https://jekyllrb.com)

日本語ページはこちら  
[https://jekyllrb-ja.github.io/](https://jekyllrb-ja.github.io)

Minimal Mistakesのインストール方法  
[https://mmistakes.github.io/minimal-mistakes/docs/quick-start-guide/](https://mmistakes.github.io/minimal-mistakes/docs/quick-start-guide/)

## 準備としてBundlerをインストールしておく
1. パッケージを更新しておく

    ```shell
$ sudo apt update
$ sudo apt upgrade
    ```
1. RubyGems(gem)を使えるようにするため、ruby-devをインストールする

    ```shell
$ sudo apt install ruby-dev
    ```
1. Bundlerをインストールする

    ```shell
$ sudo gem install bundler
    ```
1. バージョンを確認する

    ```shell
$ bundler -v
    ```

## JekyllのMinimal Mistakesテーマをインストールする手順

一般のレンタルサーバや自前のサーバ上でWebページを開設する場合はこちらの手順でインストールする

1. 適当な名前のディレクトリを作成する  
   (このディレクトリ内で一つのサイトを作成することになる)

    ```shell
$ mkdir ~/mysite
    ```
1. ディレクトリ内へ移動する

    ```shell
$ cd ~/mysite
    ```
1. Gemfileを編集する  
   (`bundle init`でフォーマットを作成することもできる)

    ```shell
$ vi Gemfile
    ```

    ```ruby
source "https://rubygems.org"
gem "jekyll", "~> 3.8.3"
gem "minimal-mistakes-jekyll"
    ```
1. インストールする

    ```shell
$ bundle install
    ```
1. バージョンやインストールされた場所などを確認する

    ```shell
$ bundle info jekyll
$ bundle info minimal-mistakes-jekyll
    ```

## Minimal Mistakesリモートテーマをインストールする手順

GitHub上でWebページを開設する場合はこちらの手順でインストールする

1. 適当な名前のディレクトリを作成する  
   (このディレクトリ内で一つのサイトを作成することになる)

    ```shell
$ mkdir ~/mysite
    ```
1. ディレクトリ内へ移動する

    ```shell
$ cd ~/mysite
    ```
1. Gemfileを編集する  
   (`bundle init`でフォーマットを作成することもできる)

    ```shell
$ vi Gemfile
    ```

    ```ruby
source "https://rubygems.org"
gem "github-pages", group: :jekyll_plugins
gem "jekyll-include-cache", group: :jekyll_plugins
    ```
1. _config.ymlを編集する

    ```shell
$ vi _config.yml
    ```
   pluginsにjekyll-include-cacheを追加する

    ```config
plugins:
  - jekyll-include-cache
    ```

1. インストールする

    ```shell
$ bundle
    ```
   `sudo bundle`にしないこと
1. バージョンやインストールされた場所などを確認する

    ```shell
$ bundle info jekyll
$ bundle info minimal-mistakes-jekyll
    ```

