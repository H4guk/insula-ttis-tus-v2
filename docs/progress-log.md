# 進捗ログ

その日の進捗を**下に追記していく**。エラーとその解決は `error-log.md`。
Obsidian 側の詳細な時系列は `myrepository/DailyLogs/`。

## 現在地（2026-11-09）
段階0（道具の確認）の 2（SimNIBS）の途中。SimNIBS 4.6.0 は入った。例の頭 ernie で charm が通るかを、GitHub Actions で確かめている（#1）。手元の Mac（16 GB）では charm の途中でメモリが足りず落ちた。

段階0の項目: 1 Mac の性能 ✅ → 2 SimNIBS（(a) 対応状況 ✅ (b) インストール ✅ (c) ernie で charm と TI ← 今ここ）→ 3 CT 付きの公開頭部データ（1回目の調べ済み）→ 4 BabelBrain・k-Wave → 5 NEURON と Aberra の錐体細胞 → 6 MorphoSONIC と PySONIC → 7 使うツールを決める。

計画の案（決定ではない）: 0 道具の確認 → 1 頭部モデルと島皮質のサブ領域 ROI → 2 tTIS の場 → 3 TUS の場 → 4 場のレベルの比較 → 5 神経（錐体細胞の tTIS → 錐体細胞の TUS。MorphoSONIC の軸索はコンテスト版の再現の照合と予備）→ 6 頭の間のばらつきと感度解析 → 7 執筆と投稿。

---

## 2026-11-05
- リポジトリ H4guk/insula-ttis-tus-v2 を作った（private）。README を最初のコミットにした。
- insula-tTIS-TUS に合わせて `.gitignore`・`requirements.txt`・`docs/`・`notebooks/`・`results/`・`scripts/` を置いた。

## 2026-11-09
- 段階0の 1（Mac の性能）: Apple M4・メモリ 16 GB・空き 314 GB。TUS の3次元計算は手元では粗い格子まで。
- 神経の比較は錐体細胞だけにすると決めた。MorphoSONIC の軸索は照合と予備に留める。
- 段階0の 2(a): SimNIBS 4.6.0 は Apple Silicon だけに対応（macOS 14.6・15.3 で試験済み）。メモリは 8 GB 必要・16 GB を強く推奨。Apple Silicon では PARDISO が動かず MUMPS を使う。TI は `TesFlexOptimization`（`max_TI`）で電極の最適化までできる。
- 段階0の 2(b): 公式の conda の手順で、conda 環境 `simnibs_env` に SimNIBS 4.6.0 を入れた（`.pkg` は使っていない）。
- 段階0の 2(c): 例のデータを `data/`（`.gitignore` 済み）に置き、手元で `charm ernie_test` を走らせたが、「Estimating cortical surfaces」の段でメモリが足りず Mac が落ちた。分割の段までは通り、骨を緻密骨（`Bone-Cortical`）と海綿骨（`Bone-Cancellous`）に分けていることを確かめた。
- 段階0の 3（1回目）: 健常者で T1・T2・CT がそろった公開データは見つからなかった。CT 付きの健常者なら CERMEP-IDB-MRXFDG（37 人・T1・FLAIR・CT・申請制）がいちばん近い。頭皮まで写っているか、使ってよい条件は未確認。
- 頭部データは「きちんと比較できること」を優先し、CT 付きを第一候補にする。CT から作った骨の形を tTIS と TUS の両方に使う。tTIS の骨は緻密骨と海綿骨の2層を主にし、CT から場所ごとの導電率を入れる方法は感度解析で試す。
- charm は手元では回さず、無料のクラウドで回す。ernie（公開データ）は GitHub Actions で試している（#1・`chore/1-charm-ernie-ci`）。申請で入手するデータは公開リポジトリのログに載せられないので、Kaggle か大学の計算機を候補にする。AWS は無料プランだと charm に足りるサーバーを使えないので外す。
