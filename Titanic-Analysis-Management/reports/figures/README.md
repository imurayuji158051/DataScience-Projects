# 📊 Figures

Titanic分析における **可視化出力・図表・グラフ** を管理します。  
学習曲線、特徴量重要度、分布比較などを保存し、成果の見える化を行います。

---

## 📁 構成（推奨例）

| ファイル名 | 内容 |
|-------------|------|
| `feature_importance.png` | 特徴量の重要度可視化 |
| `correlation_matrix.png` | 相関行列ヒートマップ |
| `learning_curve.png` | 学習・検証損失の推移 |
| `age_distribution.png` | 年齢分布ヒストグラム |
| `model_comparison.png` | モデル別スコア比較棒グラフ |

---

## 🧠 運用ポイント

- ファイル名にはバージョンまたは日付を付ける（例：`feature_importance_v2.png`）
- Notebook内の出力を自動保存（`plt.savefig("reports/figures/...")`）
- Markdownやレポートに直接貼り付ける用途を想定
