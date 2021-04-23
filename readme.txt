#------------------------------------
# ggdmvp v1.1 (2021/03/06) 
#------------------------------------

■このプログラムについて
Googleドライブにアップロードした動画ファイルをWebブラウザで連続再生するツールです。
単なるJavaScriptなので、Webサーバでも、ローカルPCでも動作します。

■パッケージ内のファイル
ggdmvp.html - Googleドライブ動画プレイヤー
index.html  - フレーム内表示のサンプル
readme.txt  - このファイル
README.md   - GitHub用のREADME

■次のページに実行例があります。
https://acax.blog.fc2.com/blog-entry-16.html
https://yuimax.github.io/ggdmvp/

■次のページにソースコードがあります。
https://bowlroll.net/file/248049
https://github.com/yuimax/ggdmvp
 
■動画の差し替え方法
表示する動画のURLやタイトルは、JavaScript中の次の配列で指定します。

	const movies = [
	  '1P0KOkdtR2dbPQdFgvfVTXkTe8q4zEXlz/10/水稀で「よくばり」',
	  '1T8g3sc00IXhnvPOe2uvMd5JTiYoUS0qt/12/AB10で「毒占欲」',
	  ：
	]

データ形式は次のとおりです。

	Googleのファイル番号 / 説明リンク用の識別キー / 動画タイトル

(1) Googleのファイル番号とは
Googleドライブにログインして、自分がアップロードした動画ファイルを右クリックし、
「リンクを取得」を選択すると、次のようなリンクが得られます。

    https://drive.google.com/file/d/1P0KOkdtR2dbPQdFgvfVTXkTe8q4zEXlz/view

この中の「1P0KOkdtR2dbPQdFgvfVTXkTe8q4zEXlz」がファイル番号です。

(2) 説明リンク用の識別キーとは
これを make_info_link() 関数に渡して、動画の説明ページへのリンクを作ります。
ご自分の環境に合わせ、適当に変更してください。

(3) 動画タイトルとは
左上の動画リストに表示される動画のタイトルです。

■ローカルPCでも動作可能
中身は単なるJavaScriptなので、ローカルPCに置いてブラウザで開けば動作します。
また、動画ファイルをGoogleドライブではなく、ローカルPCに置くこともできます。
その場合は、スクリプトを次のように修正してください。

＊ const USE_LOCAL = true; // この定数を true にする
＊ HTMLファイルと同じ場所に "video" サブフォルダを作る
＊ "video" サブフォルダに動画ファイルを入れる
＊ 個々の動画ファイル名は、動画タイトルに ".mp4" を付加したものとする

■使用条件
スクリプトの改造、流用、再配布はご自由にどうぞ。

■開発履歴
2021/02/18 v1.0 
	初期バージョン
	BowlRoll で公開
2021/03/06 v1.1
	index.htmlを追加
	GitHub でも公開

■作者
yuima
https://bowlroll.net/user/113952
https://github.com/yuimax
