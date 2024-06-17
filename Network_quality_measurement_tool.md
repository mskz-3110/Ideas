# ネットワーク品質測定ツール

## やりたいこと
- 自分が使っているネットワークのスペックが知りたい
  - RTT(Round trip time)に応じたTier
    |Rate name|Rate level|RTT range|Color|
    |:--|:--|:--|:--|
    |S|0|0 - 9ms|![](https://via.placeholder.com/16/0000ff/FFFFFF/?text=%20) Blue|
    |A|1|10 - 14ms|![](https://via.placeholder.com/16/a0d8ef/FFFFFF/?text=%20) SkyBlue|
    |B|2|15 - 19ms|![](https://via.placeholder.com/16/00ff00/FFFFFF/?text=%20) Green|
    |C|3|20 - 29ms|![](https://via.placeholder.com/16/ffff00/FFFFFF/?text=%20) Yellow|
    |D|4|30 - 49ms|![](https://via.placeholder.com/16/ee7800/FFFFFF/?text=%20) Orange|
    |E|5|50ms over|![](https://via.placeholder.com/16/ff0000/FFFFFF/?text=%20) Red|
- 自作したネットワーク通信処理の秒間通信量によるネットワーク負荷を見積もりたい
- 出力結果を他の言語やGoogleSpreadSheetで分析したい
  - 行の区切り文字
    - タブ(TSV)
      - コピーするだけでGoogleSpreadSheetの各セルに配置できる
  - 見出し
    - シンプルな行情報は[]で括る
      - Options
      - UnknownValues
    - 最初の行をキーとして扱う情報は<>で括る
      - ServerAddress
      - ClientAddress
      - Stats
    - 最初の列をキーとして扱う情報は{}で括る
      - Settings
      - Result
- 本番と同じ状況で測定したい
  - pingではなくTCPやUDPでデータ送受信を行う
- 測定を待っている間も秒単位で通信状況を確認したい
  - 通信が安定しているか判定したい
    - 1分間
- 通信状況を可視化した動画を生成したい
  - SNS投稿
    - X
    - Instagram
  - 動画形式
    - mp4
  - 動画を扱いやすい言語で作成したい
    - Python
  - グラフ
    - Y
      - Bps(Bit per second)
        - 棒グラフアニメーション
          - 色はTierColor
    - X
      - Time
    - 動画の最後にRateのスタンプアニメーション
- 様々な環境でも使えるようにしたい
  - 開発言語
    - C言語
  - 対象OS
    - Must
      - Windows
      - MacOS
      - Linux
    - Want
      - iOS
      - Android