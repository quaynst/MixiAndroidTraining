# まえがき

## Androidの基礎知識 - mixi-inc/AndroidTraining
http://mixi-inc.github.io/AndroidTraining/introductions/1.04.basic-knowledge.html

###  実習・課題
     以下の項目に取り組んでください。

1. (実習)Android SDK 内の、下記の 2 つのディレクトリにあるコマンドを列挙してください。
→ 見た
    - sdk/tools/
    - sdk/platform-tools/
2. (実習)上記のディレクトリにパスを通し、下記のコマンドを実行してください。
→ 見た
    - adb devices
    - adb shell
3. (実習)adb shellコマンドを使って、Android 内のファイルシステムにアクセスし、下記の項目を確認してください。
→ 見た
    - /data/data以下のディレクトリでlsコマンドを打っても、拒否されること
    - /sdcard/Android/data以下のディレクトリの中身を自由に読むことができること
4. (課題)adbコマンドを使って、下記の項目を実行してください（課題のファイルに、実行したコマンドを記録しておいてください）。
    - 端末のSD カード領域に、ローカルにあるファイルを転送する
    - 端末のSD カード領域から、ローカルにファイルを転送する

```sh
## PATH 通す辺りから。history の逆順になっている
adb pull /sdcard/Download/waku.txt .
adb shell
adb ssh
adb push kuwa.txt /sdcard/Download
adb push kuwa.txt
touch kuwa.txt
cd ..
cd MixiAndroidTraining/
cd work/
cd
adb devices
emacs ~/.config/fish/config.fish
echo $PATH
adb devices
fish
fg
echo $HOME
fg
pwd
emacs ~/.config/fish/config.fish
ll platform-tools/
ll tools/
ll
cd Library/Android/sdk/
cd
````

    - 課題用サンプルプロジェクトの apk ファイルをコマンド経由で端末にインストールする
    - インストールしたアプリを、コマンド経由でアンインストールする
    
# 基礎編以降は

ここ↓を clone してきて進める模様…  
git@github.com:mixi-inc/AndroidTraining.git  


---
title: 課題プロジェクトの開き方
description: このページでは、これ以降の各章での課題/実習で利用するプロジェクトの開き方について解説します。
keywords: ["android","training", "基礎", "スキル", "開発", "developer", "プログラミング", "AndroidStudio", "プロジェクト"]

---

_記述内容はAndroid Studio 2.2.2 時点のものです。_

## 目次

- [課題プロジェクトを開く](#open-projects)
- [実行](#exec)

## 課題プロジェクトを開く {#open-projects}

本リポジトリ内の `AndroidStudio/build.gradle`をAndroid Studioで開きましょう。  
開くと全課題のプロジェクト一覧がプロジェクトツリーに表示されます。

![project-view]({{site.baseurl}}/assets/01-06/open-projects.png)

これ以降の章では、このツリーに表示されるプロジェクト名に対応した、課題/実習が用意されています。

## 実行 {#exec}

それぞれのプロジェクトをビルド/実行する際は、上記スクリーンショット右上のビルドボタン(再生ボタンアイコン)の左にある、プロジェクト名のプルダウン(1-1-LinearLayoutPractice-Practice1と表示されているところ)を選択し、実行したいプロジェクトを選び、ビルドボタンを押してください。