---
title: "HugoのStackテーマでフォントを変更する"
description:
date: 2024-09-02T16:37:32Z
image:
math:
license:
hidden: false
comments: true
draft: true
---

HugoのStackテーマでフォントを変更する方法を説明します。

> ![important]
> StackテーマはHugo Moduleとしてインストーラーしたものを前提としています。

まず色々始める前に、テーマの不具合を修正します。

なぜかこのテーマ、デフォルトだとコード系（`code`, `pre`, `kbd`...）のフォントが後述の方法で変更できません。

なので、`layouts/partials/head/custom.html`に以下のコードを追加します。

```html
<style>
  pre,code,kbd,samp {
    font-family: var(--code-font-family), monospace;
  }
</style>
```
