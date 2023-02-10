## 程式簡介
程式目前功能為爬取IMDb上[即將上映電影](https://www.imdb.com/calendar/?ref_=nv_mv_cal)的部分資訊，並對其加以分析，
大部分利用Python的BeautifulSoup進行擷取網頁資訊，並用Pandas、Matplotlib產生圖表。

## 程式原理
- 取得頁面中有包含電影格子的部分的函式（如圖）

利用Python的Requests，同時也需要前面的標頭檔才能成功進入頁面。  
進入頁面後利用BeautifulSoup進行抓取頁面資訊的動作。

![image](https://user-images.githubusercontent.com/124888991/218053965-9bcf9f80-5b9d-46ac-8909-b7644622c8b6.png)
![carbon](https://user-images.githubusercontent.com/124888991/218053688-73cc0eed-db14-4e74-b2fb-f31d34219339.png)

- 取得一部電影的資訊的函式

這次想要得知的部分只有電影名稱以及類型，所以再進一步擷取想要的資訊

![carbon (1)](https://user-images.githubusercontent.com/124888991/218055893-082e95c6-989a-4601-9e7b-d5377f0ab203.png)

- 整理所得資訊

將電影名稱和類型分開存放於Python的list中，才能以Pandas的Dataframe顯示出來。  
同時，將電影類型存放於新的以多到少排序的Collections裡，Matplotlib才能畫出較直觀的圖形。
![carbon (3)](https://user-images.githubusercontent.com/124888991/218056485-b7247f3b-582a-420d-8892-f030c41d7528.png)
![carbon (4)](https://user-images.githubusercontent.com/124888991/218058083-5cbe4b63-e92c-46d7-b155-4fd0551d86c7.png)


## 程式演示
- Pandas所產生之表格

![image](https://user-images.githubusercontent.com/124888991/218058419-fa9f4d32-9a85-4bbf-aad2-8fe681882120.png)

- Matplotlib所產生之長條圖

![image](https://user-images.githubusercontent.com/124888991/218058528-7b6a214a-ae16-419f-8775-b172ae67f09a.png)
