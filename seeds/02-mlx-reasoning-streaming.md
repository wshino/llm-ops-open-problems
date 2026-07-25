# [problem] mlx_lm.server で reasoning 系モデルを serve すると streaming がクライアントを壊す

## 困っていること

Mac Studio で mlx_lm.server を立てて reasoning 系モデル (Kimi K2 系など) を OpenAI 互換 API として使うと、streaming 応答に reasoning の出力が本文と区別なく混ざり、クライアント側の解析が壊れることがあります。reasoning ブロックの区切りがモデルごとに違うのも厄介で、モデルを差し替えるたびにクライアント側の対応を書き直しています。

## 環境

- Mac Studio (Apple Silicon、メモリ 128GB 以上)
- mlx-lm の HTTP server
- Kimi K2 系、GLM 系の量子化モデル

## 試したこと

- streaming を切る。動くが体感が大きく悪化する
- クライアント側で reasoning ブロックを取り除く後処理。モデルごとの差異に追従し続ける必要がある

## どんな解決なら嬉しいか

reasoning 出力の扱いの定石。server 側で reasoning を落とす、または OpenAI の reasoning 形式に正規化するオプションや wrapper の実装例があれば知りたいです。
