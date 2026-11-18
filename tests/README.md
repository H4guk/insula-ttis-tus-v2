# tests/

`scripts/` の関数の単体テストを置く（pytest）。

- 何度も使う関数を `scripts/` に足したら、ここにテストを足す
- 頭部データや長い計算が要るものは入れない（GitHub Actions で短時間で回せるものだけ）
