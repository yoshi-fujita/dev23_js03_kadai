# 課題：　Firebaseを使ったチャットアプリ

## ① 課題内容（どんな作品か）
- 例えば、講演を聞きながらslidoでコメントを共有したり、zoomの講義でチャットでコメントする時の次の問題を解決する
  - 似たようなコメントが多数投稿され、コメントがどんどん流れていってしまう
  - 共感する人が多い重要なコメントとツマラないコメントが同列に扱われ、重要なコメントが埋もれてしまう
  - 気軽にコメントを投稿しにくい
- これらの問題を解決するために、以下の機能を提供する
  - コメントを投稿すると、画面の下部に小さく表示されるので、気軽にコメントできる
  - 共感するコメントがあれば、コメント自体をクリックするか、いいねマーク👍をクリックすることで、いいねができる
  - いいねが増えるとコメントが大きくな理、表示位置も上がってくる
- 例えば授業中に、自分だけが分からないのかも知れないと思っても、気軽に小さく呟いてみる。同じ疑問を持っている人がいいねをすると、コメントが大きくなり目立つようになる
- 上に上がってきたコメントが気に入らない場合は、「よくないね」マークをクリックすることで、下に下げることができる
- コメントには、通常コメント、疑問・質問、気づき・提案の３種類のカテゴリを用意

## ② 工夫した点・こだわった点
- Firebaseを使って、多人数で利用できるように作ったつもりだが、デプロイできていないので、多人数でのデモはまだできない
- 最初にrealtime dbをクリアする必要がある
- 最初にroom名を決めた人がadminになる。後から入る人は、同じroom名を入れないと入れない
- adminは、表示する動画のURL（YouTubeの埋め込み形式）を指定できる。例えば、https://www.youtube.com/embed/LQyNc_RBLNc

## ③ 質問・疑問（あれば）
- dbをroomごとに分けたかったが、"chat"以外にして使い分ける方法が分からなかった
- 動画を全員で同時に再生スタートさせたかったが、そこまで手が回らなかった
-　<script type="module">　以下のスクリプトを別ファイルにする方法が分からない
  
## ④ その他（感想、シェアしたいことなんでも）
- 発表直前になりましたが、デプロイに成功しました。下記のURLで、room名を「gs」にしてみてください。
- https://gs23-eb548.web.app/
