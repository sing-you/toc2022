# toc2022

Line Fitness
前言
現在健身的人愈來愈多，大家也愈來愈注重飲食健康，再加上作者本身也有健身的習慣，因此想設計一個LineChatBot來幫助有健身習慣的人，藉由它可以更清楚每天應該怎麼吃、吃多少來讓健身的效果更好。

構想
先藉由使用者輸入的性別、年齡、身高、體重、運動習慣等，幫助使用者算出BMR與TDEE。再藉由增肌、減脂兩個面向來幫助所需要的人，其中增肌有提供訓練各部位的推薦影片;減脂則是有現在主流的低醣飲食與生酮飲食來提供給大家參考。增肌、減脂都能查詢當天三大營養素應該各吃多少，也可以藉由衛生署提供的各食物營養素分析來給使用者查詢。

環境
ubuntu 18.04
python 3.6.9
技術
Olami
具有NLP的聊天機器人
Beautifulsoup4
爬取youtube各健身部位的推薦影片
使用教學
install pipenv
pip3 install pipenv
install 所需套件
pipenv install --three
// 若遇到pygraphviz安裝失敗，則嘗試下面這行
sudo apt-get install graphviz graphviz-dev
從.env.sample產生出一個.env，並填入以下四個資訊
Line
LINE_CHANNEL_SECRET
LINE_CHANNEL_ACCESS_TOKEN
Olami
APP_KEY
APP_SECRET
install ngrok
sudo snap install ngrok
run ngrok to deploy Line Chat Bot locally
ngrok http 8000
execute app.py
python3 app.py
使用說明
基本操作
所有用到英文的指令大小寫皆可
隨時輸入任何字若沒觸發到都會有提示
以下三個指令皆可隨時輸入
restart
reset所有資訊
chat
切換到聊天機器人模式
fsm
傳回當前的fsm圖片
架構圖
輸入fitness開始使用健身小幫手
輸入性別 -> 男生或女生
輸入年齡 -> 整數
輸入身高 -> 整數
輸入體重 -> 整數
輸入一週運動的天數 -> 整數
以下分成增肌與減脂來加以說明
增肌
熱量
算出BMR與TDEE
食物
可查看一天三大營養素需要吃多少
可回傳三大營養素所佔熱量比例的圓餅圖
可搜尋食物名稱來知道該食物的三大營養素
BMR
文字說明何謂BMR
TDEE
文字說明何謂TDEE
影片
會推薦youtube上的健身影片
可根據想練的部位來加以訓練
胸
背
腿
肩 (未顯示在Button上）
二頭 (未顯示在Button上）
三頭 (未顯示在Button上）
減脂
低醣飲食
熱量
算出BMR與TDEE
食物
可查看一天三大營養素需要吃多少
可回傳三大營養素所佔熱量比例的圓餅圖
可搜尋食物名稱來知道該食物的三大營養素
BMR
文字說明何謂BMR
TDEE
文字說明何謂TDEE
生酮飲食
熱量
算出BMR與TDEE
食物
可查看一天三大營養素需要吃多少
可回傳三大營養素所佔熱量比例的圓餅圖
可搜尋食物名稱來知道該食物的三大營養素
BMR
文字說明何謂BMR
TDEE
文字說明何謂TDEE
使用示範
