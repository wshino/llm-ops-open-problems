# llm-ops-open-problems

ローカル LLM や AI エージェントを実際に運用していると出てくる、誰もまとめていない未解決問題を集める場所です。

やることは 3 つだけです。

- 困っていることを issue に投げる。雑なままで大丈夫です、解ける形への整形は手伝います
- 解けそうな問題があったらコメントで解決案を書く。コード、設計案、運用事例の共有、どの形でも
- 投稿者が解決を確認したら close する。解決までの経緯は issue にそのまま残します

対象はローカル LLM の運用、AI エージェント (Claude Code、Codex CLI、各種 agent framework) の運用、その周辺ツールです。

## いま挙がっている問題

公開準備中のため、初期の問題は seeds/ に下書きとして置いています。公開時に issue 化します。

| # | 問題 |
|---|---|
| 1 | [複数の agent runner の完了通知を一元監視できない](seeds/01-agent-notification.md) |
| 2 | [mlx_lm.server で reasoning 系モデルを serve すると streaming がクライアントを壊す](seeds/02-mlx-reasoning-streaming.md) |
| 3 | [upstream の CLI 更新のたびにローカルパッチの再適用が必要](seeds/03-upstream-cli-local-patch.md) |
| 4 | [安いモデルに委譲したタスクの「本質的な見落とし」を検知できない](seeds/04-cheap-model-quality-gate.md) |
| 5 | [自律 agent loop の自己申告レポートを機械的に検証できない](seeds/05-agent-self-report-verification.md) |
| 6 | [日本語タスクに特化したローカル LLM の品質ベンチが存在しない](seeds/06-japanese-local-llm-bench.md) |
| 7 | [subscription 型 LLM の limit 逼迫を予測して routing を切り替えられない](seeds/07-limit-aware-routing.md) |

## 投稿するとき

issue テンプレートの「困っていること」だけ書けば成立します。環境や試したことは書けるところまでで大丈夫です。再現手順がまとまっていなくても、状況が伝われば整形はコメントで一緒にやります。

## 解決するとき

issue にコメントで解決案を書いてください。投稿者が試して解決を確認したら、その旨コメントして close します。誰がどう解いたかの記録が issue とプロフィールに残ります。

## この場について

報酬はありません。解いた実績と経緯が公開の場に残ること自体を価値とする場です。運営が採用や仕事の仲介をすることもありません。問題を通じて興味を持った同士が直接やりとりするのは自由です。
