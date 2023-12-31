# Webアプリに関する基礎知識（第5回特別課題）

## URLとは？
URL(Uniform Resource Locator)とは、インターネット上におけるウェブページや画像や動画などのリソースの位置を特定するための文字列。<br>
絶対URLや相対URLと呼ばれるものもある。
<br>

## クエリ文字列とは
Webブラウザがサーバーにデータを送信する際に、URLの末尾に付加する文字列のことを指す。「クエリパラメータ」とも呼ばれる。<br>
※　パラメーター＝関数に引き渡される名前付きの変数（変数の一つ？）
<br><br>
例：capybaraと検索したい場合 <br>
`https://www.google.com/search?q=capybara`<br>
？以降の文字列　→ [q=capybara] =クエリパラメータ <br>
<br>
### ・ パッシブパラメーター
表示されるコンテンツに影響は出ない。<br>
ユーザー属性を把握するための「情報収集」やWebアクセスなどの「データ解析」を目的として使用される。

### ・アクティブパラメーター
Webサイトの表示内容の変更が可能 <br>
<br>

## パスパラメーター(パス変数)とは
- 一意のリソースを指定する　→ ユーザーIDや記事のIDなど、特定の情報の表示などに活用される
- 省略は不可

## クエリ文字列とパス変数との違い
- パス変数は特定のものを判別する際に必要、省略不可
- クエリパラメーターは、特定のものに条件を追加する際に必要、省略可能
  <br>

## HTTPメソッドとは
まず、HTTPとはHTML文書などのリソースを読み取るためのもの。「HTTPリクエストメソッド」とも言われ、これらのリソースに対して実行したいアクションを示すものの一連を定義している。<br>
<br>

| **メソッド** | **意味**  |
| :----: | :------ |
GET |  データを取得 <br>送信できるデータ量に制限あり。<br>  <sub>(送信したデータがWebブラウザの履歴に残ってしまうため、機密性の保持には向かない…？)</sub>
POST | データを変更　 <br> → データ量が多い時など・PWのような秘匿情報をURL上に表示したくない場合に
PUT | 新しいリソースを作成・指定したリソースの表現の置換  <br> <sub>※連続して同じものを実行すると同じ注文を複数回してしまうなどの影響がある場合もある</sub>
PATCH | リソースを部分的に変更　<br> PUTのように他リソースに対して影響を及ぼす可能性あり　<br>アップデート
DELETE | 指定したリソースを削除

<br>
他にも、CONNECT, OPTIONS, TRACEなど様々なメソッドがある。
<br>

## HTTP（レスポンス）ステータスコード
特定のHTTPリクエストが正常に完了したかどうかを示す。
<br>

ステータスコード | Result | 意味
:---:| :---: | :---
200 | OK | リクエスト成功👏
201 | Created | リクエスト成功 & リソース作成完了
400 | Bad Request | クライアント側のエラーなどにより、リクエストの処理が出来ない　<br>（例: 構文が正しくないなど）　データに問題あり
404 | Not Found |サーバーがリクエストされたリソースを見つけることが出来ない
500 | Internal Server Error |サーバー側で処理方法がわからない事態が発生

<br>

## リクエストヘッダーとは
Webコンテンツの伝送に用いられるHTTPのこと。クライアント（Webブラウザなど）からWebサーバーへの要求内容を指す。
<br>　（例）Content-type application/fhir+json

## リクエストボディとは
クライアントからAPIにデータを送信する必要がある場合、データを「リクエストボディ」として送信する。
データを送信する際はPOST,PUT,DELETEまたはPATCHが主に使われる。

<br>

## レスポンスヘッダーとは
応答内容についての付加情報を記述したもの。サーバーからクライアントへの応答であるHTTPレスポンスの前半にある制御情報を記した領域のこと。
<br>

## レスポンスボディとは
APIがクライアントに送信するデータ。多くの場合はAPIはレスポンスボディを送らなければならない。<br>「ステータスライン」「レスポンスヘッダー」に続くHTTPレスポンスを構成する大きな部品の内の３つ目。
<br>

## JSONとは
「JavaScript Object Notation」の略称。
読み方は「ジェイソン」。<br>
<sub>（13日の金曜日に出てくるものと同じである。）</sub>
<br>

JavaScriptというプログラミング言語と相性の良いオブジェクト表記法。<br>
※「Object Notation」を直訳すると、「オブジェクトの表記方法」
<br>

<p align="right">
<img src="https://github.com/capyybara/RaiseTech_SpecialAssignment5/assets/137416338/48ef7992-dfdf-496a-9672-23e11c76d3e4" width="20%">

<br>
<br>

## JSON　映画情報 (追加課題)

```JSON 
"MovieInfo":[
  {"Movies":1, "title":"シーシャンクの空に", "director":"フランク・ダラボン", "published_year":1995}
  {"Movies":2, "title":"アナと雪の女王", "director":"クリス・バック, ジェニファー・リー", "published_year":2013}
]
```

<br>

---

## 【参考資料】
- MDN: (https://developer.mozilla.org/ja/docs/Web)
- Qiita:  [HTTPメソッド　GETとPOSTの違い](https://qiita.com/ryuuuuuuuuuu/items/94f75183bd700a8b4c15)
- ジェイソンの画像: [プリ画像](https://prcm.jp/album/nanamikalove/pic/39639402)

- わわわ: (https://wa3.i-3-i.info)







