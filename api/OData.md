## 【支援OData查詢語法】



###  基本查詢 

   http://ptx.transportdata.tw/MOTC/Rail/TRA/Station?$format={format}

   {format}為資料格式：json、xml、csv
     
   範例：火車車站基本資料http://ptx.transportdata.tw/MOTC/Rail/TRA/Station?$format=xml


| OData查詢語法 |  說明  | 範例  |
| :--: | :--------: | :--------: |
| {format} |資料格式：json、xml、csv|火車車站基本資料http://ptx.transportdata.tw/MOTC/Rail/TRA/Station?$format=xml|
|{top}|取最前筆數|火車車站基本資料 $filter={StationID}&$top=10&$format=JSON |
| {skip}|跳過筆數 |火車車站基本資料 $filter={StationID}&$skip=100&$format=JSON |
| $orderby {Field1 asc}|針對某欄位作升冪  ||
|$orderby{Field1 desc} |針對某欄位作降冪    ||
| {filter}|回傳符合特定表達式的資料   ||
|{select} | 回傳資料的某些欄位||


###  進階查詢
   
{dataId}：資料代號
   
{top}：取最前筆數
   
{skip}：跳過筆數
   
$orderby {Field1 asc}：針對某欄位作升冪 
   
$orderby{Field1 desc}：針對某欄位作降冪    
   
   + 範例：火車車站基本資料 $orderby={StationID}&$top=10&$skip=100&$format=JSON 
   
{filter}：回傳符合特定表達式的資料  
   
{select}：回傳資料的某些欄位
     
   + 範例：~火車車站基本資料 $select=StationID~
   
{and}：而且
   
{or}：或者     
   
{not}：否定     
   
{date}：日期
   
{contains}：包含
   
{all}：所有項目都要符合
   
   + 範例：針對停靠時間資料底下的車站代碼，全部的車站代碼為1000的資料就回傳  $filter=StopTimes/all(d:d/StationID eq '1000')
   
{any}：其中一項符合

   + 範例：針對停靠時間資料底下的車站代碼，任一筆的車站代碼為1000的資料就回傳 $filter=StopTimes/any(d:d/StationID eq  '1000') 


###  更多OData服務開發教學請詳見[連結](http://ptx.transportdata.tw/ptx/Download/公共運輸整合資訊平台資料服務開發實作.pdf)。
