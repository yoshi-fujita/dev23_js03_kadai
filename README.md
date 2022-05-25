# 課題：　Firebaseを使ったチャットアプリ

## ① 課題内容 - Balloon Chat（どんな作品か）
- 例えば、講演を聞きながらslidoでコメントを共有したり、zoomの講義でチャットでコメントする時の次の問題を解決する
  - 似たようなコメントが多数投稿され、コメントがどんどん流れていってしまう
  - 共感する人が多い重要なコメントとつまらないコメントが同列に扱われ、重要なコメントが埋もれてしまう
  - 気軽にコメントを投稿しにくい
  - 講師と聴講者の間のインタラクションや、聴講者間のインタラクションに繋がりにくい
- これらの問題を解決するために、以下の機能を提供する
  - コメントを投稿すると、画面の下部に小さく表示されるので、気軽にコメントできる
  - 共感するコメントがあれば、コメント自体をクリックするか、いいねマーク👍をクリックすることで、いいねができる
  - いいねが増えるとコメントが大きくなり、表示位置も上がってくる
  - これにより、普通のコメントは下を流れるが、共感者の多い重要なコメントが目立つようになり、講師の目に止まりやすくなる
- 例えば授業中に、自分だけが分からないのかも知れないと思っても、気軽に小さく呟いてみる。同じ疑問を持っている人がいいねをすると、コメントが大きくなり目立つようになる
- 上に上がってきたコメントが気に入らない場合は、「よくないね」マークをクリックすることで、下に下げることができる
- （v2　HackFes向けに改造）admin向けに「bigよくないね」ボタンを用意。これにより、回答済みの質問や、邪魔なコメントを一気に下げることができる
- コメントには、通常コメント、疑問・質問、気づき・提案の３種類のカテゴリを用意

## ② 工夫した点・こだわった点
- Firebaseを使って、多人数で利用できるように作った
- ４：３ のプロジェクタに表示しながら、上部に　１６：9のプレゼンテーション、下部にコメント欄を表示することを想定し、４：3に収まるデザインにした
- （v1　課題提出時)最初にrealtime dbをクリアする必要がある（本来は、誰でもroomを作ることができるようにする予定だった）
- （v1　課題提出時)最初にroom名を決めた人がadminになる。後から入る人は、同じroom名を入れないと入れない
- （v1　課題提出時)adminは、表示する動画のURL（YouTubeの埋め込み形式）を指定できる。例えば、https://www.youtube.com/embed/LQyNc_RBLNc
- （v2　HackFes向けに改造）誰でも新しいroomを作ってadminになることができる
- （v2　HackFes向けに改造）adminは、画像のアップロード（途中で差し替え可能）や、Youtube、画像、pdf、ページのURLを指定して表示することができる（差替え不可）
- - 名前（name）は、今後の発展用に一応入力欄はあるが、今は使っていない。匿名の投稿のみ

## ③ 質問・疑問（あれば）
- （v1　課題提出時)dbをroomごとに分けたかったが、"chat"以外にして使い分ける方法が分からなかった
- （v2　HackFes向けに改造）dbが確定した後にリスナーを定義すれば大丈夫だった
- 動画を全員で同時に再生スタートさせたかったが、そこまで手が回らなかった
- script type="module"　のスクリプトを別ファイルにする方法が分からない
- Zoom の画面にオーバーレイしたかったが、方法が分からなかった
  
## ④ その他（感想、シェアしたいことなんでも）
- 発表直前になりましたが、デプロイに成功しました
- ウィンドウの横幅が広すぎると、下部の入力領域が隠れるので、ウィンドウ幅を少し狭めてみてください。
- https://gs23-eb548.web.app/
- サンプルルーム
  - gs　（YouTuneの埋め込みURL指定）
  - image　（画像のURL指定）
  - page　（WebページのURL指定）
  - pdf　（pdfのURL指定）
  - 画像　（アップロードした画像）

![qrcode_202205252139](https://user-images.githubusercontent.com/32793942/170264116-0f39c514-19e3-4c26-8909-78323406f858.png)



