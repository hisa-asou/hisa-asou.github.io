    ---
title: "Learnテーマのインストール"
date: 2021-09-10T15:54:37+09:00
draft: true
---

## 参考: Learnテーマのサイト
  * https://github.com/matcornic/hugo-theme-learn
  
## 導入手順

* Learnテーマを適用するサイトのディレクトリを作成する。
  * どこでも良いので作業ディレクトリを作って、Git bashを開く。
  * Git bash シェルで以下を入力（サイトのフォルダ名を SampleSite とした場合）

  ```shell
  $ hugo new site SampleSite
  ```

* 作業ディレクトリ直下に "SampleSite"というディレクトリができる。
このディレクトリをここでは便宜上「ルートディレクトリ」と呼ぶ。

* 以下のようなファイル/ディレクトリが生成される

  ``` bash
  $ ls -F
  archetypes/  content/  layouts/  resources/  themes/
  config.toml  data/     static/
  
  ``` 


* Learnテーマを導入する。ルートディレクトの下にある themes ディレクトリに移動し、Git で cloneする

    ```shell
    $ cd SampleSite/themes
    $ git clone https://github.com/matcornic/hugo-theme-learn.git
    ```

* ルートディレクト直下にある  `config.toml`を編集する。

    ```toml:config.toml
    baseURL = 'http://example.org/'
    languageCode = 'ja'         # 言語コードを ja にします。
    title = 'My New Hugo Site'
    theme = 'hugo-theme-learn'  # この行を追加します。
    ```

## ローカルサーバによる表示確認

* HugoにはWebサーバ機能があるので、ルートディレクト上でそれを起動する。
  
  ```shell
  $ pwd
  /c/workdir/SampleSite
  $ hugo server -D
  ```
  
* ブラウザから、localhost:1313 にアクセスすると、デフォルトの画面が表示される。


