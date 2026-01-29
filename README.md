# Interregional Economic Analysis of the Shikoku Region (1985–2005)

## 概要
[cite_start]本プロジェクトは、1985年から2005年にわたる「地域間産業連関表」を活用し、四国地域の経済構造の変化を多角的に分析した研究リポジトリです [cite: 53]。
経済理論（産業連関分析）と現代のデータサイエンス手法（階層ベイズモデル、機械学習）を融合させ、地域経済における波及効果や構造変化の定量化を試みています。

## 研究の背景と成果
* [cite_start]**研究対象**: 1985年〜2005年の地域間産業連関表を用いた四国経済の長期構造分析 [cite: 53]。
* **主な手法**: 
    * 輸入除去処理を施した国産化行列の構築。
    * 平均波及距離（APL: Average Propagation Length）の算出による産業間結合強度の定量化。
    * [cite_start]**PyMC** を用いた階層ベイズモデリングによる地域特性の要因分解 [cite: 51, 56]。
* **学術実績**:
    * [cite_start]環太平洋産業連関分析学会（PAPAIOS）全国大会（2025年10月）発表 [cite: 53]。
    * [cite_start]土木計画学研究発表会（2025年11月）発表 [cite: 53]。
    * [cite_start]**ICES2026（国際学会）** にて可視化分析の結果を発表予定（2026年3月） [cite: 53]。

## 分析パイプライン (Analysis Pipeline)
本リポジトリは、部分的な再検証や拡張が容易な構造となっています。

1.  **[01_Data_Integration]**: 部門統合およびデータクレンジング。
2.  **[02_APL_Calculation]**: 自給率の算出および APL の計算。
    * 数理モデル: $A_{domestic} = \text{diag}(d) A_{total}$
3.  [cite_start]**[03_Bayesian_Modeling]**: PyMC による交差効果モデルの推定 [cite: 51]。
4.  [cite_start]**[04_GIS_Visualization]**: 分析結果の空間的な図示（QGIS連携） [cite: 53]。

## 技術スタック
* **Language**: Python (pandas, NumPy, scikit-learn)
* **Modeling**: PyMC (Hierarchical Bayesian Modeling)
* [cite_start]**Visualization**: Matplotlib, QGIS, Google Maps API [cite: 56]
* **Environment**: Google Colab / Local Machine

## 著者について
[cite_start]**猪田 尚希 (Inoda Naoki)** [cite: 3, 4]
[cite_start]キヤノンマーケティングジャパン株式会社 ソリューションデベロップメントセンター所属 [cite: 20, 21]。
[cite_start]横浜国立大学大学院 国際社会科学府 経済学専攻修士課程（社会人大学院）在学中 [cite: 48]。

### 専門性と実績
* [cite_start]**Academic**: 横浜国立大学経済学部を**最優秀卒業論文賞**で卒業。紀要掲載済み [cite: 60]。
* **Data Science**: 
    * [cite_start]**Kaggle Competition Expert** (Silver x1, Bronze x1) [cite: 93, 101]。
    * [cite_start]**統計検定 準1級** 合格 [cite: 101]。
* **IT Engineering**: 
    * [cite_start]**応用情報技術者** 試験合格 [cite: 101]。
    * [cite_start]**TOEIC L&R 860点** [cite: 101]。

---
> [cite_start]*"It takes all the running you can do, to keep in the same place."* > （その場にとどまるためには、全力で走り続けなければならない） [cite: 12, 13]
