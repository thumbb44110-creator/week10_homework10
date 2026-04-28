# Week 10 Homework: ARIA v7.0 — The All-Weather Auditor

## 📋 專案概況

**課程**: NTU 遙測與空間資訊之分析與應用  
**指導教授**: 蘇文瑞教授  
**作業**: Week 10 Homework  
**案例研究**: 花蓮馬太鞍溪流域 — 2025 鳳凰颱風後淹水與堰塞湖偵測

## 🎯 作業目標

建立 ARIA v7.0 全天候決策引擎，整合 SAR 雷達與光學遙測資料，實現雲層穿透能力的災害監測系統。

## 📁 專案結構

```
week10_homework10/
├── Week10_ARIA_v70_翁仕誠.ipynb          # 主要分析程式 (原版)
├── Week10_ARIA_v70_Homework_翁仕誠.ipynb # 調整後的作業版本
├── .env                                   # 環境變數設定
├── .gitignore                             # Git 忽略規則
├── Homework-Week10.md                     # 作業要求說明
├── README.md                              # 專案說明文件
└── output/                                # 輸出成果資料夾
    └── .gitkeep
```

## 🛠️ 技術架構

### 核心技術
- **STAC API**: Planetary Computer 雲端資料存取
- **Sentinel-1 RTC**: SAR 雷達資料處理
- **Sentinel-2 L2A**: 光學遙測資料處理
- **Copernicus DEM**: 地形分析資料
- **多源融合**: SAR + 光學智慧融合

### 處理流程
```
STAC 搜尋 → 資料串流 → SAR 處理 → 光學分析 → 多源融合 → 信心分級 → 決策支援
```

## 📊 四大核心任務

### Task 1: SAR 全天候淹水偵測 (25%)
- ✅ STAC 搜尋 Sentinel-1 RTC 資料
- ✅ SAR 淹水提取與斑點濾波
- ✅ 形態學清理與後處理
- ✅ 2×2 可視化面板

### Task 2: 多源感測器融合 (30%)
- ✅ 光學 NDWI 與 SAR 資料融合
- ✅ 4級信心度分類淹水地圖
- ✅ 雲層穿透能力展示

### Task 3: DEM 地形分析 (20%)
- ✅ DEM 地形展示與坡度計算
- ✅ 地形適用性討論
- ✅ 與淹水分佈的關聯分析

### Task 4: AI 決策簡報與比較分析 (25%)
- ✅ AI 生成的策略簡報準備
- ✅ 與 Week 9 光學結果比較
- ✅ 系統效能評估

## 🔧 環境設定

### 必要套件
```bash
pip install numpy matplotlib scipy xarray rioxarray
pip install pystac-client planetary-computer stackstac
pip install python-dotenv geopandas
```

### 環境變數 (.env)
所有參數已設定在 `.env` 檔案中，包括：
- 研究區 BBOX 座標
- 時間範圍設定
- SAR/NDWI/坡度閾值
- STAC API 設定

## 📈 預期輸出

### 視覺化成果
- `W10_Task1_SAR_Flood_Detection.png` - SAR 淹水偵測 2×2 面板
- `W10_Task1_SAR_Histogram.png` - SAR 反散射直方圖
- `W10_Task2_Sensor_Fusion.png` - 多源融合信心圖
- `W10_Task3_Topographic_Analysis.png` - 地形分析對比圖

### 分析報告
- AI 策略簡報與反思
- Week 9 vs Week 10 比較分析
- DEM 適用性討論

## ⚠️ 重要注意事項

### 嚴格禁止事項
- ❌ 任何形式的模擬資料
- ❌ 跳過驗證步驟
- ❌ 本地檔案下載處理

### 技術要求
- ✅ 必須使用 STAC API 雲端串流
- ✅ 災前災後軌道方向必須一致
- ✅ 所有輸出必須經過合理性檢查

### 學術責任
- 確保所有結果的物理合理性
- 提供完整的方法論解釋
- 記錄所有關鍵決策的理由

## 🚀 執行方式

1. **環境準備**
   ```bash
   cd week10_homework10
   pip install -r requirements.txt  # 如有需要
   ```

2. **執行分析**
   ```bash
   jupyter notebook Week10_ARIA_v70_Homework_翁仕誠.ipynb
   ```

3. **逐步執行所有 cells**
   - 按順序執行每個程式碼區塊
   - 觀察輸出結果與視覺化圖表
   - 確認所有數據的合理性

## 📝 繳交清單

- [x] Jupyter notebook (`Week10_ARIA_v70_翁仕誠.ipynb`)
- [x] `.env` 環境設定檔
- [x] 所有 4 個任務的完整實作
- [x] STAC 搜尋結果列表
- [x] 災前災後軌道方向一致性確認
- [x] 專業呈現：清晰的 markdown、圖表、表格
- [x] Captain's Log 說明
- [x] DEM 適用性討論
- [x] AI 簡報包含個人反思
- [x] Week 9 vs Week 10 比較表格
- [x] 程式碼可重現性

## 🏆 技術成就

### 創新突破
- **全天候監測**: SAR 確保惡劣天氣下的監測能力
- **高精度偵測**: 與實測資料高度一致的結果
- **信心分級**: 提供不確定性評估
- **智慧融合**: SAR 與光學優勢互補

### 實務價值
- **防災決策**: 高信心區域優先處理
- **資源優化**: 根據信心度分配應急資源
- **風險管理**: 提供多層次決策資訊

---

**The Captain's Final Thought:**
"A commander doesn't care if it's cloudy. He needs the truth. ARIA v7.0 delivers it."

*Week 10 Homework Complete — ARIA v7.0 All-Weather Auditor Operational*
