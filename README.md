# Cat-Meeting
■サービス概要

Cat-Meetingは、自分と相性の合う猫を教えてくれ、出会いの機会を与えてくれるアプリです。
相性の合う猫と出会う診断系サービスで、飼い主と猫をマッチさせます。
また、近所で譲渡会や捨て猫等があれば、メールで通知がもらえます。

■ このサービスへの思い・作りたい理由

私自身幼い頃から猫を飼ってきたため、辛いことや落ち込んだりしたときは、癒しをもらいながら生活してきました。
実際に猫を飼うことで、心身の健康を保ち、健康寿命まで伸びると言われています。
しかし、近所では捨て猫や野良猫が多く、食べ物や水分を摂れない猫がたくさんいます。
私自身も保護猫活動のボランティアに参加していますが、資金や人手に限界があり、多くの猫が亡くなるのを目の当たりにしてきました。
そんな悔しさと無念から、一匹でも多く家庭に引き取ってもらい家族の一員として、猫も人も幸せになれる社会になってほしいと思い、アプリを制作しました。

■ ユーザー層について
猫を飼いたい全ての世代の人
理由、、、一匹でも多くの猫の命を救うため。飼い猫か野良猫で健康寿命に３〜５倍近くの乖離がある事実もある。
普段の生活で疲れやストレスを感じやすい人
理由、、、猫を見たり触れることで、ストレスが軽減され気分向上につながるため。
心身の健康を維持し、円満に長く生きたい人
理由、、、体調が整い、血圧、コレステロール、血糖値を下げる効果があるため。


■サービスの利用イメージ
ユーザーはアプリに会員登録を行い、簡単な質問に答える。質問内容は、ライフスタイルや好み、猫に求める性格を回答する。
ユーザーは、譲渡会や捨て猫があったとき、自分にぴったりの猫を見つけることができ、飼った後もお互いに楽しく過ごせる確率が高まる。
また、猫との相性が良いことで、ストレスの軽減や癒しを得ることができ、生活の質が向上する

■ ユーザーの獲得について

SNS（InstagramやX）で猫のかわいい写真や動画を投稿し、より多くのユーザーの興味を引く。
ファミリー向けのイベントや地域の猫関連の催しに参加し、直接アプリを紹介する。

■ サービスの差別化ポイント・推しポイント

他のサービスは一般的な猫の種類を紹介するだけのことが多いが、個々のユーザーに対して特化したアンケートを行うことで、より高い満足度を実現し、期待に沿った猫を紹介できるようにしている。
またログインすることで、ユーザー同士が交流できるコミュニティ機能を提供しており、飼い方や猫の健康に関する情報を共有できる。

■ 機能候補

MVPリリース時に作っていたいもの、、、トップページ、ユーザー登録機能、ログイン機能、質問に基づくマッチング機能、猫の一覧ページ、猫の詳細ページ、写真投稿機能、掲示板（猫）投稿機能
ページネーション機能

本リリースまでに作っていたいもの、、、コミュニティ（チャット）機能、コメント機能、いいね機能、専門家アドバイス機能、猫の健康管理機能、検索機能、位置情報機能（地図表示機能）、LINE通知機能、マルチ検索・オートコンプリート、レビュー（レーティング）機能、ソート機能


■ 機能の実装方針予定

写真投稿機能、、、CarrierWaveを使用して画像をアップロードし、AWS S3を利用する。同時に投稿された画像に対して、AIを使った画像解析を行い、猫の写真であるかどうかを判断する仕組みを導入する。
また投稿時に「猫」カテゴリを選んでもらい、ユーザーが「猫」を選ばなかった場合、その投稿を拒否する仕組みを作る。

マルチ検索・オートコンプリート機能、、、Stimulus Autocompleteでユーザーの希望する猫の条件の入力を減らす。

コミュニティ（チャット）機能、、、WebSocketを利用してリアルタイムでメッセージを送受信できるようにする

位置情報機能、、、Geocoderを用い、譲渡会の会場や捨て猫がいる位置を表示する。

LINE通知、、、LINE Messaging API SDK for Rubyを使用し、LINEでも通知が来るように実装する。

専門家アドバイス機能、、、ユーザーが質問を投稿し、専門家がそれに回答する機能を実装する。

マッチング機能:、、、ユーザーの回答に基づいて、猫の種類を提案するアルゴリズムを作成する。
１.あらかじめ、猫の種類とその特徴を含むデータベースを作成し、ユーザーの価値観や好みにあう猫を登録しておきます。
２.ユーザーの回答を分析し、ユーザーの好みや価値観を抽出し、データベースから関連する猫の種類を複数ピックアップします。
３.技術的に可能であれば、ユーザーの過去の選択を学習するモデルを導入し、よりパーソナライズされた提案ができるように検討します。