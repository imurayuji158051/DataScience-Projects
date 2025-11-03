# Titanic-Analysis-Management
Titanic機械学習コンペの分析・管理ログ（Feature設計・性能記録・提出管理などを含む）

---

# 🚢 Titanic - Machine Learning from Disaster

### *Analysis & Management Logbook*

---

## 📘 概要（Overview）

このプロジェクトは、Kaggle公式コンペ
👉 [**Titanic - Machine Learning from Disaster**](https://www.kaggle.com/c/titanic)
を題材に、**データ分析・特徴量設計・モデル構築・改善サイクル**を体系的に記録・管理することを目的としています。

学習目的は「**再現性のある実験と構造的な分析管理**」。
単なるスコア競争ではなく、**思考過程（仮説 → 検証 → 改善）を記録して共有可能な形にする**ことを目指します。

---

## 🎯 プロジェクト目標

| 項目          | 内容                                                         |
| ----------- | ---------------------------------------------------------- |
| **タスク種類**   | 二値分類（Binary Classification）                                |
| **目的変数**    | `Survived`（0 = 死亡, 1 = 生存）                                 |
| **評価指標**    | Accuracy                                                   |
| **最終目標スコア** | 0.800以上                                                    |
| **到達目標**    | 上位10%（約0.80〜0.81）                                          |
| **活用技術**    | Python, Pandas, Scikit-learn, RandomForest, Colab, Excel連携 |

---

## ⚙️ ディレクトリ構成

```
Titanic-Analysis-Management/
│
├── README.md                           ← このファイル
│
├── data/                               ← Kaggle提供データ
│   ├── train.csv
│   └── test.csv
│
├── notebooks/                          ← 分析ノート（Google Colab対応）
│   ├── 01_EDA.ipynb                    # 探索的データ分析
│   ├── 02_FeatureEngineering.ipynb     # 特徴量加工
│   ├── 03_Modeling.ipynb               # 学習・予測
│   └── 04_Evaluation.ipynb             # 精度検証・提出ファイル作成
│
├── reports/                            ← 成果物・記録ファイル
│   ├── Titanic_Analysis_Management_Logbook.xlsx   # Excel管理台帳
│   ├── figures/                        # グラフ・出力画像
│   └── submissions/                    # Kaggle提出ファイル
│
└── utils/                              ← スクリプト群
    ├── preprocessing.py
    ├── train_model.py
    └── evaluate.py
```

---

## 🧭 学習サイクル（再現可能な実験手順）

| ステップ         | 内容                                           | 成果物                                        |
| ------------ | -------------------------------------------- | ------------------------------------------ |
| ① 問題設定       | 目的・評価指標・データ確認                                | `README.md`（本ファイル）                         |
| ② データ理解（EDA） | 欠損・分布・相関の可視化                                 | `01_EDA.ipynb`                             |
| ③ 特徴量設計      | 「項目設計」シートに仮説を記録                              | `Titanic_Analysis_Management_Logbook.xlsx` |
| ④ モデル構築      | Logistic Regression / RandomForest / XGBoost | `03_Modeling.ipynb`                        |
| ⑤ 検証・改善      | 「性能記録」シートに結果を記録                              | `Titanic_Analysis_Management_Logbook.xlsx` |
| ⑥ 提出         | Kaggleへ送信（Public/Private差異を記録）               | `/reports/submissions`                     |
| ⑦ 振り返り       | 改善ログ・スコア推移まとめ                                | `/reports/figures`                         |

---

## 📊 管理台帳（Excel連携）

### 🧩 シート構成

| シート名                     | 内容                 |
| ------------------------ | ------------------ |
| **概要**                   | コンペ基本情報・進行状況・目標管理  |
| **項目設計（Feature Design）** | 各特徴量の意味・加工・欠損・効果   |
| **性能記録（Evaluation Log）** | 実験ID・モデル設定・スコア履歴   |
| **改善ログ（今後追加）**           | 仮説→検証→改善サイクルを短文で記録 |
| **提出履歴（今後追加）**           | 提出ファイルとスコアの対応表     |

> 📍 Excelは `/reports/Titanic_Analysis_Management_Logbook.xlsx` に格納
> GitHub上ではCSV変換版を置いてもOK。

---

## 📈 現在の進捗（例）

| レベル     | 内容                      | スコア   | 状況        |
| ------- | ----------------------- | ----- | --------- |
| Level 1 | Logistic Regression（基礎） | 0.765 | ✅ 完了      |
| Level 2 | RandomForest（Title追加）   | 0.789 | ✅ ベース構成確立 |
| Level 3 | 相互作用特徴量（Age×Title）      | 0.770 | ⚠ 過学習傾向   |
| Level 4 | GridSearch最適化           | 0.763 | ⚠ 効果薄     |
| Level 5 | RF+XGBアンサンブル            | 0.758 | ❌ 精度低下    |
| Level 6 | Fare_log＋Age補完安定化       | 0.795 | 🚧 改善中    |

---

## 🧠 改善ログ（例）

| 試行ID   | 改善内容          | 結果      | 学び             |
| ------ | ------------- | ------- | -------------- |
| EXP002 | Title特徴追加     | ✅ +0.03 | 社会的地位の情報が有効    |
| EXP003 | Age×Title補完導入 | ⚠ 過学習   | データ量とのバランス重要   |
| EXP005 | アンサンブル導入      | ❌ 精度低下  | 少データでの多モデルは非効率 |

---

## 💡 今後の課題と展望

* [ ] Age補完の階層化（Groupby＋Title改善）
* [ ] Feature Importance可視化で寄与度分析
* [ ] 学習曲線を用いた汎化性能確認
* [ ] Notebook自動化（パイプライン構築）
* [ ] 次コンペ（House Prices / Titanic Transfer Learning）への応用

---

## 🧰 使用技術

| 分類          | 使用ツール・技術                                         |
| ----------- | ------------------------------------------------ |
| **言語**      | Python (3.10+)                                   |
| **主要ライブラリ** | pandas, numpy, matplotlib, seaborn, scikit-learn |
| **環境**      | Google Colab / Jupyter Notebook                  |
| **モデル**     | LogisticRegression, RandomForest, XGBoost        |
| **バージョン管理** | GitHub / GitHub Desktop                          |
| **記録管理**    | Excel（Feature設計・性能記録）＋ Markdown（README）          |

---

## 🏁 成果まとめ（更新予定）

* **現在最高スコア（Public LB）**：0.795
* **目標スコア**：0.800
* **到達状況**：安定構成確立＋次フェーズ（欠損処理・最適化）へ移行
* **今後の方向性**：Titanicをベースに「構造化されたデータ分析管理テンプレート」を確立し、他コンペへ展開予定。

---

## 🪄 Author

**Yuji Imura（井村 勇士）**
📍 Data Science / Learning Design / AI Education
📫 [LinkedIn](https://www.linkedin.com/in/yuji-imura-90bb182a9/) | [Note](https://note.com/imurayuji) | [GitHub](https://github.com/imurayuji158051)

---

### 📄 License

This project is licensed under the **MIT License** — see the [LICENSE](./LICENSE) file for details.

---

## 💬 補足

> このREADMEは、単なる結果報告ではなく、
> **「思考の再現性」**を重視した記録フォーマットです。
> チーム学習・教育・キャリア支援などへの応用も想定しています。

---
