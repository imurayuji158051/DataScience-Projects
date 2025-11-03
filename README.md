# 🎯 DataScience-Projects
機械学習・深層学習・統計分析など、AI・データサイエンスに関する学習・実践プロジェクトを体系的に管理するための統合リポジトリです。  
すべてのプロジェクトで共通構造・共通管理テンプレートを採用し、学びと実践を再利用可能な形で記録します。

---

## 🧭 目的

- Kaggle・人工知能などの学習内容を、実務的な形で整理・発信する
- 分析プロセス（Input → Process → Output → Feedback）を統一管理する
- 自分や他者が再現可能な学習プロジェクトテンプレートを構築する

---

## 📂 プロジェクト一覧

| No | プロジェクト名 | 主な目的 | 使用技術 | 進捗状況 | ノートブック |
|----|----------------|-----------|-----------|-------------|---------------|
| 1 | [Titanic-Analysis-Management](./Titanic-Analysis-Management) | 分類入門（生存予測） | Python, pandas, scikit-learn | 🟢 進行中 | [01_EDA.ipynb](./Titanic-Analysis-Management/notebooks/01_EDA.ipynb) |
| 2 | [FashionMNIST-Classification](./FashionMNIST-Classification) | 深層学習（Softmax・MLP） | PyTorch, NumPy | 🟢 実施中 | - |
| 3 | [HousePrice-Prediction](./HousePrice-Prediction) | 回帰予測 | LightGBM, Feature Engineering | 🔵 準備中 | - |

---

## 🧩 共通テンプレート

- [`Shared-Templates/kaggle_setup.ipynb`](./Shared-Templates/kaggle_setup.ipynb)  
  → Kaggleデータの安全な取得・環境構築用
- [`Shared-Templates/project_structure_template.xlsx`](./Shared-Templates/project_structure_template.xlsx)  
  → データ分析・特徴量設計・スコア管理表
- [`Shared-Templates/model_evaluation_sheet.xlsx`](./Shared-Templates/model_evaluation_sheet.xlsx)  
  → 精度・過学習・パラメータ比較を記録

---

## 🧠 管理ポリシー

| 項目 | 方針 |
|------|------|
| **データ** | 公開データのみ扱う（機密データは含めない） |
| **APIキー類** | GitHubにはアップロードせず、Google Driveなど非公開領域に保存 |
| **ファイル命名** | `01_`, `02_`, `03_` のように手順順に整理 |
| **成果物** | スコア・学び・改善案を`reports/`内にまとめる |
| **学習サイクル** | Input → Process → Output → 再入力（再循環モデル）を適用 |

---

## 🧾 更新履歴

| 日付 | 内容 |
|------|------|
| 2025-11-03 | Titanic分析フォルダを統合構成に移行 |
| 2025-11-04 | READMEテンプレート（全体版）作成 |
| 2025-11-05 | 他プロジェクト（FashionMNIST, HousePrice）準備予定 |

---

## 👤 作者

**井村勇士 (Yuji Imura)**  
- AI × 教育 × 社会設計をテーマに活動中  
- 問題と向き合える社会をつくるための「学びの再循環モデル」を研究  
- [GitHub](https://github.com/imurayuji158051) ｜ [Note](https://note.com/) ｜ [LinkedIn](https://linkedin.com/) ｜ [Kaggle](https://www.kaggle.com/)

---

## 🪪 License
This project is licensed under the MIT License.
