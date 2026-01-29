# Interregional Economic Analysis of the Shikoku Region (1985–2005)

## 概要
本プロジェクトは、1985年から2005年にわたる「地域間産業連関表」を活用し、四国地域の経済構造の変化を多角的に分析した研究リポジトリです。
経済理論（産業連関分析）と現代のデータサイエンス手法（階層ベイズモデル、機械学習）を融合させ、地域経済における波及効果や構造変化の定量化を試みています。

## 研究の背景と成果
* **研究対象**: 1985年〜2005年の地域間産業連関表を用いた四国経済の長期構造分析。
* **主な手法**: 
    * 輸入除去処理を施した国産化行列の構築。
    * 平均波及距離（APL: Average Propagation Length）の算出による産業間結合強度の定量化。
    * **PyMC** を用いた階層ベイズモデリングによる地域特性の要因分解。
* **学術実績**:
    * 環太平洋産業連関分析学会（PAPAIOS）全国大会（2025年10月）発表。
    * 土木計画学研究発表会（2025年11月）発表 [cite: 53]。
    * **ICES2026（国際学会）** にて可視化分析の結果を発表予定（2026年3月）。

## 分析パイプライン (Analysis Pipeline)
本リポジトリは、部分的な再検証や拡張が容易な構造となっています。

1.  **[01_Data_Integration]**: 部門統合およびデータクレンジング。
2.  **[02_APL_Calculation]**: 自給率の算出および APL の計算。
    * 数理モデル: $A_{domestic} = \text{diag}(d) A_{total}$
3.  **[03_Bayesian_Modeling]**: PyMC による交差効果モデルの推定。
4.  **[04_GIS_Visualization]**: 分析結果の空間的な図示（QGIS連携）。

## 技術スタック
* **Language**: Python (pandas, NumPy, scikit-learn)
* **Modeling**: PyMC (Hierarchical Bayesian Modeling)
* **Visualization**: Matplotlib, QGIS
* **Environment**: Google Colab
