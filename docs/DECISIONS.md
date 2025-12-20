# Decision Log

## 2025-12-20 — PR Size Labeler を追加

- 決定: PR の行数に基づく `size/XS`〜`size/XL` ラベル付与を実装。
- 理由: 迅速に PR の相対的な作業量を判断できるため。実装は `.github/workflows/pr-size-label.yml`。
- 閾値: XS <10, S <50, M <200, L <500, XL >=500
- 実装メモ: `git diff --numstat base...head` で追加・削除を合算して算出。既存のサイズラベルは削除して最新を付与する。

## 今後の記録ルール

- 重要な設計変更や閾値の調整はこのファイルに日付・決定内容・理由・関連ファイルを追記する。
