# 📦 Data

Titanic分析で使用する **入力データ・派生データ・中間生成物** を管理します。  
このフォルダには、Kaggle公式の `train.csv` / `test.csv` をはじめ、  
前処理済みデータ・特徴量抽出後のデータを保存します。

---

## 📁 構成（推奨例）

| ファイル名 | 説明 |
|-------------|------|
| `train.csv` | 学習用データ（目的変数含む） |
| `test.csv` | テストデータ（目的変数なし） |
| `gender_submission.csv` | Kaggle公式のサンプル提出データ |
| `train_preprocessed.csv` | 前処理・欠損補完後の学習データ |
| `features_selected.csv` | 特徴量選択・変換後のデータ |

---

## ⚠️ 管理ルール

- 公開可能なデータのみアップロード可（Kaggle公式データのみ）
- 個人APIキー・外部データ・個人情報を含むデータは禁止
- 大容量データは `.gitignore` に追加（Git LFS不要）

---

## 💡 Tips
データの前処理履歴や加工方法は  
`notebooks/02_Preprocessing.ipynb` に記録してください。
