# ネットワークゲームの問題点

## マッチング
- マッチングに時間がかかる
  - 10秒以内にマッチングしたい
- マッチング精度が低い
  - 自分と同じ実力の人とマッチングしたい
    - 実力が異なる人と対戦するのは勉強になるが初心者が離脱しやすくなる
  - 自分と同じfpsが出る人とマッチングしたい
    - ノートPCを充電していない状態だとfpsが落ちることを知らずにマッチングしてしまい、対戦相手に迷惑をかけた
  - 有線と無線のマッチングを分けたい
    - 有線側が不利になりやすい

## 通信エラー
- 対戦中にエラーが発生すると対戦がなかったことにされる
  - 対戦情報を端末にキャッシュしておき、通信できるようになったタイミングでサーバーに情報を送ることで解決
  - 有名なゲームでも対応できてないので、おそらく費用面の問題で難しいと思われる
    - 買い切り型だと毎月のサーバー代を賄うための収益化が難しいので、無駄な通信は極力抑えたい
- 通信エラーによるペナルティは百害あって一利なし
  - 通信エラーの原因がどこにあるか特定できないため、悪質ユーザーを特定するのが難しい
    - 誤ってペナルティを与えた場合、正規ユーザーのゲーム体験を損ねる
      - そのゲームを嫌いになり、プレイしなくなる
  - 対戦中にエラーが発生してもサーバーに情報を残すようにしておけば、負けそうになったからわざと通信エラーを引き起こしたのか判断しやすくなる