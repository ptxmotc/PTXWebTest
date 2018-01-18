## 【支援OData查詢語法】



###  基本查詢 

   http://ptx.transportdata.tw/MOTC/Rail/TRA/Station?$format={format}




| OData查詢語法 |  說明  | 範例  |
| :--: | :--------: | :--------: |
| {format} |資料格式json、xml、csv|火車車站基本資料<br>$format=xml</br>|
| {filter}|回傳符合特定表達式的資料   |$filter={StationID}|
|{select} | 回傳資料的某些欄位||
|{top}|取最前筆數|火車車站基本資料 <br>$filter=$top eq 10&$format eq JSON</br> |
| {skip}|跳過筆數 |火車車站基本資料 <br>$filter=$skip eq 100&$format eq JSON</br> |
|{and} | 而且  ||
| {or}|或者 ||
| {not}| 否定  ||
|{date} |日期 ||
| {contains}| 包含  ||
| {all}| 所有項目都要符合|針對停靠時間資料底下車站代碼，全部的車站代碼為1000的資料就回傳 <br> $filter=StopTimes/all(d:d/StationID eq '1000')</br>|
| {any}|  其中一項符合 |針對停靠時間資料底下車站代碼，任一筆的車站代碼為1000的資料就回傳 <br>$filter=StopTimes/any(d:d/StationID eq  '1000')</br> |
| | ||
| orderby {Field asc}|針對某欄位作升冪  ||
|orderby{Field desc} |針對某欄位作降冪    ||






###  更多OData服務開發教學請詳見[連結](http://ptx.transportdata.tw/ptx/Download/公共運輸整合資訊平台資料服務開發實作.pdf)。
