# 進捗ログ

その日の進捗を**下に追記していく**。エラーとその解決は `error-log.md`。
Obsidian 側の詳細な時系列は `myrepository/DailyLogs/`。

## 現在地（2026-11-05）
リポジトリを作り、ファイル構成を整えた。次は段階 0（道具の確認）。

計画の案（決定ではない）: 0 道具の確認 → 1 頭部モデルと島皮質のサブ領域 ROI → 2 tTIS の場 → 3 TUS の場 → 4 場のレベルの比較 → 5 神経（錐体細胞の tTIS → 錐体細胞の TUS。MorphoSONIC の軸索はコンテスト版の再現の照合と予備）→ 6 頭の間のばらつきと感度解析 → 7 執筆と投稿。

---

## 2026-11-05
- リポジトリ H4guk/insula-ttis-tus-v2 を作った（private）。README を最初のコミットにした。
- insula-tTIS-TUS に合わせて `.gitignore`・`requirements.txt`・`docs/`・`notebooks/`・`results/`・`scripts/` を置いた。

## 2026-11-09
- 段階0の 1（Mac の性能）: Apple M4・メモリ 16 GB・空き 314 GB。TUS の3次元計算は手元では粗い格子まで。
- 神経の比較は錐体細胞だけにすると決めた。MorphoSONIC の軸索は照合と予備に留める。
