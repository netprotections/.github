# Benefit (なぜmergeが必要なのか)
<!--
価値(Benefit)を生まないPull Requestはmergeされる必要がありません。
- 紐づくGithub Issue, Scrapbox Pageはなにか
  - 「なぜ必要なのか」はできる範囲で事前に議論し尽くしましょう
  - ほぼ必ず、必要性を議論した資料/chat/議事録があるはずなので、しっかり要約して、本Pull Requestに明記してください
- 対処したいBugはなにか
- 追加したい機能はなにか
- なぜ対処/追加する必要があるのか
- 他の実装方法はなかったか。なぜ他の実装方法ではなく、この実装方法にしたのか
- 必ず「Benefitを要約した内容」がPull Request titleになるように、Titleを変更してください。
  - titleだけで「なぜ必要で、どんな変更をするのか」がわかるように工夫をしてください。
-->
${issue URL}のためのPull Request
- ${理由}のため、${変更内容}したい
  - 理由の詳細1
    - 理由のevidence 1
    - 理由のevidence 2
  - 理由2
- ${理由}のため、${変更内容}したい

# Side Effect (既存systemへの副反応はあるか)
<!--
全ての変更において「Benefit」を生み出す前に、「既存systemへの副反応(悪影響)を防ぐ」必要があります。
- そもそもsystem的にどんな変化が生まれるのか
- その変化は、どんな本番影響を起こすのか
  - 障害を起こさないか？
  - User体験が変わらないか？
-->
- system影響
  - ${理由}のためsystem影響は${影響範囲}に${影響量}と判断している
    - 影響
      - ${mergeすることで起こる変化}を通して、${systemに起きる影響}が発生しうる
    - 対策
      - 予防
        - 予防の仕方1
        - 予防の仕方2
      - リカバリー
        - リカバリーの仕方1
        - リカバリーの仕方2
  - ${理由}のためsystem影響は${影響範囲}に${影響量}と判断している
    - 影響
    - 対策

- user影響
  - ${理由}のためUser体験への影響は${影響する人}に${影響量}と判断している
    - 影響
      - ${mergeすることで起こる変化}を通して、${User体験の変化}が発生しうる
    - 対策
      - 予防
        - 予防の仕方1
        - 予防の仕方2
      - リカバリー
        - リカバリーの仕方1
        - リカバリーの仕方2


# Verification (BenefitとSide Effectをどう検証したか)
<!--
検証(verification)が出来なければmergeが出来ません。
- どんな環境で検証したのか？
  - この環境は本番環境と同じと捉えて良いものか
- 検証は具体的にどんな手順で行ったのか
  - reviewerが全く同じcheckが行えるように
  - 検証結果も端的に記載しましょう
  - 理想の手順はTestを作り、Pull Reqesut作成したら自動でverificationされることです
-->

- ${検証方法と検証結果の要約}を通して、問題なしと判断
  - 検証方法
    - Step1
      - 明快な作業手順
      - 実施の結果
    - Step2
      - 明快な作業手順
      - 実施の結果
    - Step3
      - 明快な作業手順
      - 実施の結果

# References (その他 Pull Requestの意義・内容を理解する上で必要な資料はあるか)
<!--
本Pull requestについて理解したい人は、この概要から全ての資料/情報にaccessできるようにしましょう
- Pull request作成までの作業手順書・logがあれば必ず添付しましょう
-->

- 作業log
  -
- Pull Request作成までの参考資料
  -
  - 


# TakeOver (申し送り,引き継ぎ事項, knowledge)
<!--
Codeには残らない設計思想等や、ちょっとした工夫があれば必ず記載しましょう
- 選択肢がある上で意思決定したもの、悩んだものはなにか
  - どんな選択肢があったのか
  - なぜ今回は他の選択肢を選ばなかったのか
- 今までのPull Request, 開発の流れとは違うけど、やってみたことはなにか
  - なぜその工夫をしたのか
-->


# Check list (Pull Request Mergeまでの手順)
- Pull Requestのreview依頼をするまで
  - [ ] 本Pull Request概要を作成する
  - [ ] 関連資料 (特に作業log)をrefactoringして、knowledge (特にerror出たもの,選ばなかった他の選択肢)が他memberにも行き渡るようにする
  - [ ] verification（自動testを含む）を行い、Benefit/Side Effectともに想定通りであることを確認する
  - [ ] Pull Request編集画面でreviewerを指定し、Slackで連絡をする
- Pull Request Mergeするまで
  - [ ] 不明なところ,曖昧なところは質問と議論を重ね、明らかにしていく
  - [ ] 質問と議論の結果を反映させて、みんなでPull Request概要を作り上げる
