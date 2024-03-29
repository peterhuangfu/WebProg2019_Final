# 107-2 Web Final Project
## (Group 1) Online Music Converter

## 一句話描述這個 Project
將音樂檔轉成樂譜的線上轉換功能

## Github Repo
https://github.com/peterhuangfu/WebProg2019_Final.git

## 操作 / 使用說明
### Installation
```
git clone
cd WebProg2019_Final && npm install
cd front-end && npm install
cd ../back-end && npm install
```
### Run
Front end
```
cd WebProg2019_Final/front-end
npm start
```
Back end
```
cd WebProg2019_Final/back-end
node server.js
```

## 其他說明
1. 首先很抱歉，因為轉譜的 server 是架在別人的電腦上，但沒辦法一直開著，所以請助教要測試的時候先跟我們說一下，等我們把 server 打開 & 重新推github (因為我們使用 ngrok，所以每次打開都會更換網址)後再 clone 下來做測試。  

2. 上傳 WAV 之前需要去 google 商店下載 Allow-Control-Allow-Origin Plugin 並打開，網址如下： https://chrome.google.com/webstore/detail/allow-control-allow-origi/nlfbmbojpeacfghkpbjhddihlkkiljbi?hl=zh-TW  

3. 因為轉譜的演算法還在持續精進中(現在還沒有到很好)，所以這邊提供一個簡單的雙聲道 WAV 檔做測試，網址如下： https://drive.google.com/open?id=1hlmCL4hNVffd1g3k0vhCj8GnpP1gPqJH  

4. 雖然有 deploy 到 heroku 上面，但是上傳音檔及下載 PDF 的部分會有不知名原因導致失敗，這部分礙於時間還來不及解決，因此可以當作沒有deploy QQ  

## 使用之第三方套件 / 框架 / 原始碼
Front end — React + Material UI  
Back end — Node.js + Express + MongoDB  
轉譜的 Server — Django [特別感謝鄭揚、蔡涵如同學的幫忙]  

## Demo
Youtube：https://www.youtube.com/watch?v=nrVDhs5fIUM  

## Deployed Repo
https://luluwebfinal.herokuapp.com/  

## 分工
#### 皇甫立翔：
所有前端部分，幫忙後端研究 PDF 下載的部分。  

#### 劉韋成：
後端的大部分 API 功能。例如：註冊、登入、回傳個人資訊、檔案資訊。PDF 的儲存、下載回傳為共同研究。  

#### 顏价廷：
幫忙研究 PDF 的儲存以及下載的部分。  

## 心得
#### 皇甫立翔：
期中後學到了 Redux 和 GraphQL，都是神器等級的好用工具，結果被大量的 project 淹沒，沒時間好好研究應用在這次的 final project，覺得很可惜 QQ，以後一定會多花時間去熟悉。  

這次我負責全部的前端及幫忙研究後端傳輸檔案，由於之前去實習面試被噴炸版的問題，所以這次大部分的介面有稍微去處理這個問題，絕大部分用 flex 及 % 去處理這部分，好像稍微好點了(汗)。前端的部分不外乎就是資料的 handle 以及繁瑣的 css，即使用了 Material-UI，要自己更改 style 仍然是一件非常麻煩的事。這次比較特別的是要處理 WAV 檔的傳送及傳輸、下載 PDF 的部分。WAV 在做傳輸的時候一開始不知道要怎麼處理，結果丟過去的檔案直接變成一團尖銳的雜音，後來才設定成非壓縮檔傳過去才解決。PDF 也是相當的麻煩，必須兩邊都設定相同的傳輸 type 才能 work，即使這樣，有時候存進資料庫明明都是好的檔案，結果下載下來的檔案打開都顯示損毀(崩潰)，這部分真的花了很多的心力，即使到了現在也還沒辦法保證 100% 成功 QQ。  

最後很高興能修到這門課，學了越多，越發現自己的能力是多麽不足 QQ，感謝教授及助教的辛苦付出，也感謝我的組員讓我在很崩潰的時候沒有真的崩潰，也感謝一起研究轉譜的同學，還免費幫我們架 server，身邊到處都是貴人啊 QQ。  

#### 劉韋成：
在修這堂課以前，我沒有使用過框架，也沒有寫過後端例如 Node.js，只用過 pure.js 寫過一些簡單的網頁，所以一開始接觸的時候真的是一直碰壁，一邊查資料一邊覺得心好累。這份 final project，我的工作主要是處理 server 的 api 和 mongoDB 的連動。在研究將檔案傳入 DB 的時候，就發生了寫程式的人十之八九都會遇到的問題 : 花了老半天，卻沒有任何進度。那個時候真的內心崩潰哈哈!  
  
當然，最後還是順利解決了，而我也領悟到了一些道理 : 雖然現在仍然是鼓勵大家使用 open source 大於自己從頭用手刻，但如果只是一味複製貼上的話，沒有出問題只是代表自己非常非常的幸運，真正去了解它運作的過程，才是讓專案能夠更有效率完成的最大好的方法(雖然最後也是從別人那裏去改哈哈)。  
  
學期初聽到教授對同學們的放話(?)也是感到震懾，也很慶幸我能夠撐到最後。最後，謝謝這門課讓我學到很多實用的技術，希望未來我也能夠善用我這學期的收穫。  

#### 顏价廷：
首先要感謝教授把期末報告的死線延後，不然一堆報告的情況下真的是吐血。  
  
整學期下來其實對整個 react 架構非常的清楚，照期中的模式其實要完成一個期末很簡單，因此我們想要做一點突破，除了後端與前端還多了一個 server 需要介接。整個前端的部分，託 material-UI 的福我們節省了很多調校的時間。而這個系統的功能需要讓客戶端下載與上傳檔案，也因此資料傳輸的部分，從前端到伺服器再到後端，幾乎大部分的研究都花在該如何使一份完整的檔案透過正確的方式完整的傳輸，stackoverflow 真的是救星。  
