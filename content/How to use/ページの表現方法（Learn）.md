---
title: "ページの表現方法（Learnテーマ）"
date: 2021-09-10T16:53:07+09:00
draft: true
weight: 50
---

### Capter

* 章の扉のページをそれらしい体裁で生成
* 以下のコマンドを実行

  ```shell
  $ hugo new --kind chapter <name>/_index.md
  ```
  
* content/<name>/_index.md が生成される。以下のような Front Matterが付く

  ``` toml
  +++
  title = "<name>"
  date = 2021-09-28T14:27:04+09:00
  weight = 5
  chapter = true
  pre = "<b>X. </b>"
  +++
  
  ### Chapter X
  
  # Some Chapter title
  
  Lorem Ipsum.
  ```

* 章番号や説明文などで上書きする。

  ``` toml
  +++
  title = "Introduction"
  date = 2021-09-28T14:27:04+09:00
  weight = 5
  chapter = true
  pre = "<b>1. </b>"
  +++
  
  ### Chapter 1
  
  # Introduction
  
  Hugoの紹介をします。
  ```

参照→[章見出しのページサンプル]({{< ref "/introduction/_index.md" >}})


