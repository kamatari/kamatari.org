---
title: "Generate Site With Hugo and Host on Netlify"
date: 2018-01-28T14:26:10+09:00
draft: false
---
# Overview
HugoとNetlifyを使ってこのサイトをつくったので、その時のメモ。

# Hugo Settings
公式サイトで何も不自由はないかも。

+ [Hugo Quick Start](https://gohugo.io/getting-started/quick-start/)

config.tomlはこんな感じに。

```
baseURL = "https://kamatari.org/"
languageCode = "ja"
title = "kamatari.org"
theme = "temple"
```

# Netlify Settings
![Netlify](/img/netlify.png)

Hugoのドキュメントに、Netlifyでホスティングする方法が書いてあるので、ますはそこを確認。

+ [Hugo Hosting on Netlify](https://gohugo.io/hosting-and-deployment/hosting-on-netlify/)

基本的にはドキュメント通りで問題はないが、一点だけ、localで動かしているHugoのバージョンをNetlify側で指定しないとBuildに失敗する現象が起きた。

メニューのBuild & Deploy -> Build environment variables で、以下の設定を行う。

```
key = HUGO_VERSIONS
value = 0.31.1
```

Build & Deploy設定
```
Build command = hugo --theme=temple
Publish directory = public
Production branch = master
```

## 独自ドメインの設定 + SSL

こちらのblogを参考にさせていただいた。

[NetlifyとGithubで独自ドメインのサイトをHTTPS化したメモ](http://magcho.hatenablog.jp/entry/2017/10/15/023440)

Let's Encryptのおかげで、簡単にSSLを有効にできる便利さに感動。

![Lets Encrypt](/img/lets_encrypt.png)

以上
