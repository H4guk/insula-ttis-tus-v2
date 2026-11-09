# insula-ttis-tus-v2

[English](README.md)

ヒトの島皮質に対する、時間干渉刺激（tTIS）と経頭蓋超音波刺激（TUS）の比較の論文版です。

コンテスト版（Sim4Life Student Competition 2026・Sim4Life.lite の頭部モデル1体・末梢の軸索）は [H4guk/insula-tTIS-TUS](https://github.com/H4guk/insula-tTIS-TUS) にあります。このリポジトリでは、その版の限界を直すために、オープンなツールで比較をやり直します。

- 頭部モデルを1体から複数にする
- 両手法で同じ頭部モデルと同じ神経シミュレータを使う
- 末梢の軸索ではなく、皮質の錐体細胞を使う

予定のツール（未確認）: SimNIBS（頭部モデル・tTIS の場）、BabelBrain か k-Wave（TUS の場）、NEURON と Aberra の皮質の神経細胞、PySONIC（神経の反応）。

論文の神経の比較は、皮質の錐体細胞だけで行います。MorphoSONIC の軸索は、新しいパイプラインがコンテスト版の結果を再現するかの照合と、TUS で錐体細胞がうまくいかないときの予備に使い、結果としては出しません。

### 構成

```
.github/         git のルール（CONTRIBUTING.md）・Issue/PR のテンプレート・PR の形式チェック
docs/            進捗ログ・エラーログ・方法のノート・図
notebooks/       解析の notebook
results/         小さな結果の表（大きな場の出力はコミットしない）
scripts/         パイプラインと解析のスクリプト（scripts/README.md を参照）
requirements.txt 後処理で使う Python パッケージ
```

頭部データ（MRI・CT）、SimNIBS の頭部メッシュ、場の出力はコミットしません（`.gitignore` を参照）。
