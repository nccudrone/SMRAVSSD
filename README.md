# SMRAVSSD：郊區、山區道路俯視角空拍影像語意切割資料集 (Suburban、Mountain Road Aerial View Senmantic Segmentation Dataset)

## Overview
此資料集為台灣郊區、山區道路俯視角空拍語意切割資料集。  
由政大無人機團隊 StarLab 使用 DJI Mavic2 Zoom 進行收集與標註。  
收集範圍經緯度為24.9792 ~ 24.9769, 121.5673 ~ 121.5729。  
錄製角度可以分為俯視(攝影機向下90度)與前視(攝影機向下16度)，飛行高度在5 ~ 30公尺之間。  

資料集內有兩個資料夾：img、label，裡面各有10部影片資料夾，VIDEO_0000 ~ VIDEO_0006為俯視，VIDEO_0007 ~ VIDEO_0009為前視。  
img/ 為原始圖像，檔案類型為.jpg。  
label/ 為遮罩圖與標註檔案，檔案類型為.png與.json。  
* 遮罩圖僅標註道路部分。  
* 遮罩圖為二進位png檔案，像素值0表示非道路，像素值1表示道路。
* 標註檔案使用labelme進行道路標註，以描邊方式將道路部分框住。
* 標註檔案內記載資訊如下：  
  * shapes：描邊資料結構  
  * shapes/label：描邊標註類別，此處統一為 "road"
  * shapes/points：描邊多邊形座標
  * shapes/shape_type：描邊種類，統一為 "polygon"
  * imagePath：原始圖像檔名
  * imageHeight：原始圖像高
  * imageWidth：原始圖像寬

下面為部分預覽影像，左邊為原始圖像，右邊為遮罩圖(像素值0以紫色表示，像素值1以黃色表示)：  
<img src="https://github.com/nccudrone/SMRAVSSD/blob/main/image/roadlabel1.png" width="856" height="240"/> 
<img src="https://github.com/nccudrone/SMRAVSSD/blob/main/image/roadlabel2.png" width="856" height="240"/><br/>
## Notes  
* 此資料集為郊區、山區道路俯視角空拍語意切割資料集的一部分，做為免費開放使用
* 此資料集用於學術研究
* 此資料集可以應用如[albumentations](https://github.com/albumentations-team/albumentations "link")進行影像擴增來加強訓練
* 此資料集包含原始圖像、遮罩與標註檔案，原始影像檔案請參考：[repo](https://github.com/nccudrone/SMRAVVD "link")
## Download
[link](http://140.119.164.183:5000/sharing/iwq6R7xNI "link")
## Licence
請參考 [LICENSE](https://github.com/nccudrone/SMRAVSSD/blob/main/LICENSE "link")
