# Shikoku Economic Analysis (1985–2005)

## Project Overview
1985年から2005年までの20年間、計5時点の地域間産業連関表を用いた四国地域の経済構造分析プロジェクトです。
バブル経済から低成長期への移行という劇的な変化の中で、地域内の産業構造がどのように変容したのかを、経済理論とデータサイエンスの両面から定量化しています。

## Research Background & Novelty
* **20年間にわたる長期時系列分析**
  地域間産業連関表を用いた分析の多くは単一時点の断面的分析ですが、本研究では20年分の一貫した部門統合を行い、時系列での構造比較を実現しました。この規模の長期分析は、先行研究においても類を見ない取り組みです。
* **産業間結合の質的評価**
  単なる取引額の推移ではなく、後述するAPL（平均波及距離）を用いることで、産業間の「繋がり方」の変容を抽出しています。
* **統計モデリングの導入**
  決定論的な分析に留まらず、PyMCによる階層ベイズモデルを導入。地域固有の要因と全国的なトレンドを分離して推定しています。

## Methodologies
### 1. APL (Average Propagation Length)
産業間の「経済的な距離」を測定する指標です。ある部門への需要が、何段階（何部門）を経て対象部門に波及するかを算出します。
* **Intuition**: 物理的な距離ではなく、波及の「ステップ数」を可視化。
* **Insight**: 四国地域におけるサプライチェーンの効率化、あるいは結びつきの希薄化を定量的に捉えます。

### 2. Localization Process
地域外への経済漏出を考慮し、輸入（域外流入）を控除した国産化行列を構築。
* **Model**: $$A_{domestic} = \text{diag}(d) A_{total}$$
* 地域内での真の経済波及効果を測定するための必須工程として実装しています。

### 3. Hierarchical Bayesian Modeling
PyMCを用い、地域間波及構造の要因分解を実施。

## Analysis Pipeline
1. **Data Preparation**: 1985-2005年の部門統合、統計データのクレンジング。
2. **Structural Analysis**: 輸入除去処理およびAPLの算出。
3. **Statistical Inference**: 階層ベイズモデルによるパラメータ推定。
4. **Visualization**: 分析結果の空間的な図示（QGIS連携）。

## Academic Presentations
* **PAPAIOS（環太平洋産業連関分析学会）** 第36回大会（2025年10月）
* **第72回 土木計画学研究発表会**（2025年11月）
* **ICES2026（13th International Conference on Economic Structures）** 発表予定（2026年3月）

## Technical Stack
* **Language**: Python (pandas, NumPy, scikit-learn)
* **Modeling**: PyMC
* **GIS**: QGIS, Google Maps API
* **Platform**: Google Colab
