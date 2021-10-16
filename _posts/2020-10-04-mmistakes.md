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

### Jekyllの公式サイト
* [https://jekyllrb.com/](https://jekyllrb.com)

日本語ページはこちら

* [https://jekyllrb-ja.github.io/](https://jekyllrb-ja.github.io)

## 準備としてBundlerをインストールする手順
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

## Jekyllをインストールする手順
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

   テーマは`Minimal Mistakes`を使用する

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
  * jekyll (3.8.7)
        Summary: A simple, blog aware, static site generator.
        Homepage: https://github.com/jekyll/jekyll
        Path: /var/lib/gems/2.5.0/gems/jekyll-3.8.7
$ bundle info minimal-mistakes-jekyll
  * minimal-mistakes-jekyll (4.19.2)
        Summary: A flexible two-column Jekyll theme.
        Homepage: https://github.com/mmistakes/minimal-mistakes
        Path: /var/lib/gems/2.5.0/gems/minimal-mistakes-jekyll-4.19.2
    ```
