# 📨 Submissions

Kaggleへの提出ファイル（`submission.csv`）およびその履歴を管理します。  
スコア推移を可視化し、改善効果を記録します。

---

## 📁 構成（推奨例）

| ファイル名 | 内容 |
|-------------|------|
| `submission_v1.csv` | 最初の提出結果（ベースライン） |
| `submission_v2.csv` | 改善後モデルの提出結果 |
| `submission_best.csv` | 現時点のベストスコア提出 |
| `submission_log.xlsx` | 提出履歴・スコア・メモ |

---

## 🧠 記録の観点

| 項目 | 内容 |
|------|------|
| 提出日 | Kaggleに提出した日付 |
| CVスコア | Cross-Validationでのスコア |
| LBスコア | Kaggle Leaderboard上のスコア |
| 変更点 | 特徴量・モデル・パラメータの主な違い |

---

## 📈 改善サイクル例

1️⃣  モデル更新（`03_Modeling.ipynb`）  
2️⃣  CV評価結果確認  
3️⃣  提出（`05_Submission.ipynb`）  
4️⃣  スコアを `submission_log.xlsx` に追記  
5️⃣  グラフとして `reports/figures/` に保存
