# Competition_2020_Mango_Image_Recognition-Defective_Classification
AI CUP 2020 Mango Image Recognition Challenge: Defective Classification

<img src="./figures/title.PNG" width = "800" height = "150" div align=center />

## 比賽說明

- 此項比賽希望AI圖像識別技術能夠應用於圖像分類，快速識別愛文芒果有缺陷的原因。此外，希望這些數據將來能用於分析和預測，為生產者提供信息，降低芒果的次品率。

- 訓練資料：25768張

- 測試資料：7363張

- 不良品類別：乳汁吸附(Adsorption)、機械傷害(Mechanical damage)、炭疽病(Anthrax)、著色不佳(Poor coloring)、黑斑病(Black spot)

## 操作說明

**程式碼與相關資料集都在此[google drive](https://drive.google.com/drive/folders/1Y80QSO-BmjAg1w6DNExpaxfzKL5_w1J_?usp=sharing)取得**

* 資料集

1. 訓練資料集在mango_data/txt/images/train2017裡

2. 測試資料集在mango_data/yolov5_self/data/images裡

* 執行程式

1. 訓練指令如下：
  ```
  python train.py --weights yolov5x.pt --batch-size 24 
  ```
  
2. 測試(偵測)指令如下：
  ```
  python detect_modify.py --weights best.pt –conf 0.1 --augment 
  ```
  
* 其他文件說明

1. yolo_txt_process.py / yolo_txt_process.ipynb →

  是將圖片路徑寫入txt檔以及將圖片的類別和位置資訊以yolov5規定的格式寫入txt檔

2. test_result_label.py / test_result_label.ipynb →

  是將test圖片偵測後輸出的結果轉換為各自包含的不良類別，並將答案填回特定的csv檔案中

## 實驗結果

<img src="./figures/mango.png" width = "800" height = "150" div align=center />
