# 🌍 ClimateHealthRisk: 天氣變數與健康風險分析

## 📖 專案簡介
本專案探討 **各種天氣相關變數對健康風險指標的影響**，透過 **EDA（探索式資料分析）** 找出關鍵變數，並使用 **機器學習模型** 來預測健康風險。研究數據來自美國多個城市的氣象與空氣品質數據，透過模型比較與解釋，找出最具影響力的變數，並分析其對健康風險的影響。

## 🔥 研究動機
隨著 **極端氣候與空氣汙染問題日益嚴重**，天氣對健康的影響越來越值得關注。本專案希望透過數據分析與機器學習方法，找出影響健康風險的主要天氣因子，進一步協助公共衛生與決策制定。

## 📊 數據集與研究方法
### **📂 資料來源**
- 數據集來自 [Kaggle](https://www.kaggle.com/datasets/abdullah0a/urban-air-quality-and-health-impact-dataset/data)
- 包含 **1000 筆數據**，涵蓋 **氣溫、濕度、風速、降水、太陽輻射、UV 指數** 等 46 個變數

### **🔍 研究方法**
1. **探索式資料分析（EDA）**
   - 缺失值處理
   - 目標變數分佈分析
   - 數值變數與健康風險的關聯分析
   - 相關係數熱力圖
2. **特徵工程**
   - **風速比率**（最大風速 / 平均風速）
   - **城市 Target Encoding**
   - **二元變數處理**（是否為週末）
3. **機器學習模型建構**
   - 使用 **PyCaret** 進行自動化模型選擇
   - 訓練 **SVM、Random Forest** 等模型
   - 透過 **Accuracy、AUC、Recall、Precision、F1-score** 進行評估
4. **模型解釋性**
   - **SHAP** 分析特徵影響力
   - **特徵重要性分析**

## 🏆 研究結果
- **影響健康風險的關鍵因素**
  1. **露點溫度（Dew Point）**
  2. **熱指數（Heat Index）**
  3. **雲量覆蓋率（Cloud Cover）**
  4. **氣壓（Pressure）**

- **最佳模型：Random Forest**
  | 模型 | Accuracy | AUC | Recall | Precision | F1 |
  |------|----------|------|--------|----------|----|
  | **Random Forest** | **0.84** | **0.76** | **0.89** | **0.81** | **0.85** |
  | SVM | 0.82 | 0.74 | 0.87 | 0.79 | 0.83 |

- **SHAP 分析結果**
  - 露點溫度（Dew Point）對健康風險影響最大
  - 熱指數、氣壓、雲量覆蓋率為重要特徵
  - 高溫高濕的天氣條件通常導致更高的健康風險

## 🚀 未來展望
- **擴展數據**：增加不同國家與地區的氣象與健康數據
- **提升模型解釋性**：測試更多特徵工程方法，如 One-Hot Encoding、Embedding
- **應用於公共衛生領域**：開發氣象健康風險預測系統，提供決策建議

## 🔧 技術與工具
- **Python**（pandas、numpy、matplotlib、seaborn）
- **機器學習**（PyCaret、Random Forest、SVM）
- **數據預處理**（Target Encoding、特徵選擇）
- **模型解釋性**（SHAP）

## 📂 專案結構
📂 ClimateHealthRisk   
│── 📄 README.md # 本文件   
│── 📄 ClimateHealthRisk.pdf # 研究報告 PDF 版本   
│── 📄 ClimateHealthRisk_code.ipynb # Jupyter Notebook (完整數據分析)  
│── 📄 ClimateHealthRisk_report.pdf # 簡報  
│── 📄 Quality_Dataset.csv # 原始數據   


## 📜 參考資料
- [Kaggle 數據集](https://www.kaggle.com/datasets/abdullah0a/urban-air-quality-and-health-impact-dataset/data)
- [Alberta 空氣品質健康指數](https://www.alberta.ca/about-the-air-quality-health-index)
- [NOAA 熱指數](https://www.weather.gov/ama/heatindex)
- [紫外線指數解釋](https://www.cwa.gov.tw/Data/knowledge/announce/service13.pdf)

