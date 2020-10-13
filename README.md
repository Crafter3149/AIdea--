# AIdea--
DNN-LSTM-XGboost-FCN

資料包含
Train.csv
Train_log.csv
Test.csv
Test_log.csv
submission

.csv使用PID與log.csv進行對應

DNN 不理想的結果

Train.csv、Train_log.csv 經過相關性分析後，丟入大量特徵至ＤＮＮ中，並使用網站提供的Loss Function (Wmae)獲得了一個不理想的結果

LSTM  +  DNN 上傳結果之一 採用_DiFF資料上傳
將log.csv資料按照時間序列輸入至LSTM中，.csv資料輸入至DNN中，在使用Keras(Merge)功能將兩個Model的神經元輸出項連接，並在下方接入一個MLP，輸出預測目標
學會了Keras組合Model的方式(Keras新版中已刪除Merge連結Sequence的用法)
FCN  +  DNN  不理想 速度較LSTM快

XGboost 最佳的結果　採用Ｘ資料上傳
簡單的使用相關性篩選結果後，建立４個Xgboost預測4個目標，便能獲得良好的結果
