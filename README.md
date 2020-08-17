# tensorflowJS
此源碼參考tensorflow/tfjs-models
https://github.com/tensorflow/tfjs-models

##

# 說明
#### (1)本處修改前台的src呼叫，直接指定版本，並免網頁讀取model失敗  
##### <script src="https://cdn.jsdelivr.net/npm/@tensorflow/tfjs@0.9.0">
##### <script src="https://cdn.jsdelivr.net/npm/@tensorflow-models/coco-ssd@1.1.0">
    
  ##
  
#### (2)bbox屬性
##### const result = await model.detect(image);
##### ....
##### 此處result是辨識結果物件bbox，具備以下三個屬性~
##### [{
  ##### bbox: [x, y, width, height],
  ##### class: "cat",
  ##### score: 0.8380282521247864
##### }]  

  
 ## 
  
#### (3)多個bbox
##### bbox輸出若有3個，result[i]的i會是0,1,2，分別代表三個bbox
##### result[0].bbox, .class, .score
##### result[1].bbox, .class, .score
##### result[1].bbox, .class, .score
