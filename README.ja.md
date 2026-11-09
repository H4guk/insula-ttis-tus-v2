# insula-ttis-tus-v2

[English](README.md)

ヒトの島皮質に対する、時間干渉刺激（tTIS）と経頭蓋超音波刺激（TUS）の比較の論文版です。

コンテスト版（Sim4Life Student Competition 2026・Sim4Life.lite の頭部モデル1体・末梢の軸索）は [H4guk/insula-tTIS-TUS](https://github.com/H4guk/insula-tTIS-TUS) にあります。このリポジトリでは、その版の限界を直すために、オープンなツールで比較をやり直します。

- 頭部モデルを1体から複数にする
- 両手法で同じ頭部モデルと同じ神経シミュレータを使う
- 末梢の軸索ではなく、皮質の錐体細胞を使う

予定のツール（未確認）: SimNIBS（頭部モデル・tTIS の場）、BabelBrain か k-Wave（TUS の場）、NEURON と Aberra の皮質の神経細胞、PySONIC（神経の反応）。

論文の神経の比較は、皮質の錐体細胞だけで行います。MorphoSONIC の軸索は、新しいパイプラインがコンテスト版の結果を再現するかの照合と、TUS で錐体細胞がうまくいかないときの予備に使い、結果としては出しません。

## リポジトリ構成

```
insula-ttis-tus-v2/
├── README.md            # 英語版の README
├── README.ja.md         # 本ファイル（日本語版）
├── LICENSE              # MIT
├── requirements.txt     # 後処理用の Python パッケージ（予定のツールはコメントで記載）
├── .gitignore           # 頭部データ（MRI・CT）/ SimNIBS のメッシュ / 場の出力 / 秘密情報 を除外
├── .github/             # git のルール
│   ├── CONTRIBUTING.md              # Issue・branch・commit・PR・レビューの書き方
│   ├── ISSUE_TEMPLATE/              # Issue のテンプレート [Bug] / [改修] / [作業] / [アイデア]
│   ├── PULL_REQUEST_TEMPLATE.md     # PR のテンプレート
│   └── workflows/pr-format-check.yml  # PR のタイトルと見出しを確かめる
├── scripts/             # パイプラインと解析のスクリプト
│   ├── README.md                    # どのスクリプトがどの段階のものか
│   └── archive/                     # 一度きりの調査・検証（履歴として保存）
├── notebooks/           # 解析ノートブック
├── docs/                # 進捗ログ・エラーログ・方法のノート
│   ├── progress-log.md
│   ├── error-log.md
│   └── figures/
└── results/             # 小さな結果の表（大きい場の出力は .gitignore）
```

頭部データ（MRI・CT）、SimNIBS の頭部メッシュ、場の出力はコミットしません（`.gitignore` を参照）。

## ライセンス

このリポジトリで公開する独自の内容には [MIT License](LICENSE) を適用します。このリポジトリと組み合わせて使う他者のツールや頭部データは含めておらず、それぞれのライセンスに従います。
