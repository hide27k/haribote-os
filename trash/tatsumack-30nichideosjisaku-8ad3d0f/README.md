# 『30日でできる！ OS自作入門』 for MacOSX

『30日でできる！ OS自作入門』川合 秀実氏(著)の開発環境をMacでも扱えるようにします。ここの通りにすればWindowsとほぼ同等の環境を用意できるので、Macでも本書の内容に沿って学習を進めていくことが可能です。

## 動作環境

以下の環境で正常に動作確認を行っています。

- OS
	- Mac OS X El Capitan 10.11.2

## 環境構築手順

### 1. 必要なものをインストール&用意

1. `HariboteOS`という名前のディレクトリをホームディレクトリに作成
 	- `mkdir ~/HariboteOS`
2. [サポートサイト](https://book.mynavi.jp/supportsite/detail/4839919844.html)からCDイメージをダウンロードし、`projectsディレクトリ`と`tolsetディレクトリ`をさっき作成した`HariboteOSディレクトリ`にコピー
3. tolsetOSXをダウンロード
 	1. ダウンロードページ→[http://shrimp.marokun.net/osakkie/wiki/tolsetOSX/](http://shrimp.marokun.net/osakkie/wiki/tolsetOSX/)
 	2. tolsetOSX-070221.dmgという名前のファイルをダウンロードして解凍
 	3. 解凍したデータのうち`z_toolsディレクトリ`を`HariboteOSディレクトリ`にコピー
4. qemuをダウンロード
	1. `brew install qemu`
	2. `qemu-system-i386 -version` でバージョンを確認
		- (現時点でバージョンは`2.5.0`)

#### HariboteOSのディレクトリ構造

最終的に下記のような構造になっていれば問題無いです。

- ホームディレクトリ
	- HariboteOS
		- projects(付属CD-ROMのやつ)
		- tolset(付属CD-ROMのやつ)
		- z_tools(tolsetOSXのやつ)

### 2. シェルスクリプト実行

` curl https://raw.githubusercontent.com/tatsumack/30nichideosjisaku/master/bin/install.sh | sh `

### 3. 確認

```
cd ~/HariboteOS/01_day/helloos0  
make run
```

実行して以下のように表示されていれば成功です。

![image](https://github.com/sandai/30nichideosjisaku/raw/master/bin/img/qemu.png)

## URL

- [「30日でできる！ OS自作入門」のサポートページ](http://hrb.osask.jp/)
	- 公式サポートサイト
- [tolsetOSX](http://shrimp.marokun.net/osakkie/wiki/tolsetOSX/)
	- Mac版のtolset配布ページ
- [0xED](http://www.suavetech.com/0xed/0xed.html)
	- バイナリエディタ配布サイト
	
