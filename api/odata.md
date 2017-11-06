# 【ODATA使用說明】

1. 基本查詢
     http://ptx.transportdata.tw/MOTC/Rail/TRA/Station?$format={format}

     {format}為資料格式：json、xml、csv

     範例：火車車站基本資料http://ptx.transportdata.tw/MOTC/Rail/TRA/Station?$format=xml


2. 進階查詢


     {dataId}：資料代號

     {format}：資料格式

     {top}：取最前筆數

     {skip}：跳過筆數

     {orderby}：排序欄位

     範例：火車車站資本資料

     http://ptx.transportdata.tw/MOTC/v2/Rail/TRA/Station?$orderby=StationID&$top=10&$skip=100&$format=JSON 

     ps：其中StationID為資料欄位名稱

3. ODATA服務開發實作請詳見[連結](http://ptx.transportdata.tw/ptx/Download/公共運輸整合資訊平台資料服務開發實作.pdf)。
