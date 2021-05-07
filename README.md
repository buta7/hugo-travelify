# README

## セットアップ

サイト作成

```shell
hugo new site hugo-traverify
```

レポジトリ初期化

```shell
cd hugo-traverify
git init
echo '*~' >> .gitignore
echo '*.bak' >> .gitignore
echo '*.orig' >> .gitignore
echo '.env' >> .gitignore
echo 'public' >> .gitignore
echo 'resources' >> .gitignore
```

テーマ設定

```shell
git submodule add https://github.com/balaramadurai/hugo-travelify-theme.git themes/traverify
```

サイト設定
g
```shell
cp -pr themes/hugo-traverify/exampleSite/{content,static,config.toml} .
```

config.toml

```toml
baseURL = "https://buta7.github.io/hugo-traverify/"
languageCode = "ja"
title = "Hugo Traverify"
#publishDir = "docs"
#themesDir = "../.."
paginate = 6
```

> github pagesやnetlifyで使う場合はbaseURLのプロトコルはhttpsにすること

Githubレポジトリ作成後

```shell
cp somplace/Makefile
git remote add origin git@github.com:buta7/hugo-traverify.git
git add .
git commit -m 'init'
git push -u origin main
```

## Github Actionsの利用

* .github/workflows/gh-pages.yamlを作成
  * ソースはmainブランチ
  * 出力はpublicフォルダの内容をgh-pagesブランチ
    * Github>Settings>Gighub Pages>Source>gh-pages branch

## 既存のレポジトリからクローンする場合

```shell
git clone git@github.com:buta7/hugo-traverify.git hugo-traverify
cd hugo-traverify
git submodule update --init --recursive
```

## 使い方

### 投稿

新規投稿

```shell
hugo new posts/hello.md
content/posts/hello.md created
```

編集

```shell
vi content/posts/hello.md
```

## Link

* [Hugo Travelify Theme \| Hugo Themes](https://themes.gohugo.io/hugo-travelify-theme/)
