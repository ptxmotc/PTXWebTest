## 【支援OData查詢語法】



###  基本查詢 

   http://ptx.transportdata.tw/MOTC/Rail/TRA/Station?$format={format}




| OData查詢語法 |  說明  | 範例  |
| :--: | :--------: | :--------: |
| format | 資料格式json、xml、csv | 回傳xml格式<br>$format=xml</br> |
| filter | 回傳符合特定表達式的資料 | 車牌號碼等於636-U7的資料<br>$filter=PlateNumb eq '636-U7'</br> |
| select | 回傳資料的某些欄位 | 回傳欄位1<br>}?$select= Field1</br >|
| top | 取最前筆數 | 火車車站基本資料取前10筆 <br>$top=10</br> |
| skip | 跳過筆數 | 火車車站基本資料跳過前100筆 <br>$skip=100</br> |
| eq | 等於 | 車牌號碼等於636-U7的資料<br>$filter=PlateNumb eq '636-U7'</br> |
| ne | 不等於| 行車狀況不等於正常的資料<br>$filter=BusStatus ne '正常'</br> |
| gt | 超過| 行駛速度超過100的資料<br>$filter=Speed gt 100</br> |
| ge | 大於 | 行駛速度大於100的資料<br>$filter=Speed ge 100</br> |
| lt | 不及 | 行駛速度不及100的資料<br>$filter=Speed lt 100</br> |
| le | 小於 | 行駛速度小於100的資料<br>$filter=Speed le 100</br> |
| and | 而且 | 行駛速度不及100而且行車狀況不等於正常的資料<br>$filter=Speed lt 100 and BusStatus ne '正常</br> |
| or | 或者 | 行駛速度不及100或是行車狀況不等於正常的資料<br>?filter=Speed lt 100 or BusStatus ne '正常'</br> |
| not | 否定 | 車牌號碼的結尾 不為U7的資料<br>$filter=not endswith(PlateNumb,'U7')</br> |
| add | 加 | 行駛速度加2等於102 的資料<br>$filter=Speed add 2 eq 102</br> |
| sub | 減 | 行駛速度減2等於102 的資料<br$filter=Speed sub 2 eq 102></br> |
| mul | 乘 | 行駛速度乘2等於102 的資料<br>$filter=Speed mul 2 eq 102</br> |
| div | 除 | 行駛速度除2等於102 的資料<br>$filter=Speed div 2 eq 102</br> |
| mod | 餘數 | 行駛速度除2的餘數等於2的資料<br>$filter=Speed mod 2 eq 2</br> |
| date | 日期 | 資料紀錄時間的日期格式為2015-09-17的資料<br>$filter=date(UpdateTime) eq  2015-09-17</br>  |
| contains | 包含 | 車牌號碼為包含的FA的資料<br>$filter=contains(PlateNumb, 'FA')</br> |
| all | 所有項目都要符合|針對停靠時間資料底下車站代碼，全部的車站代碼為1000的資料就回傳 <br> $filter=StopTimes/all(d:d/StationID eq '1000')</br> |
| any | 其中一項符合 | 針對停靠時間資料底下車站代碼，任一筆的車站代碼為1000的資料就回傳 <br>$filter=StopTimes/any(d:d/StationID eq  '1000')</br> |
| orderby {Field asc} | 針對某欄位作升冪 | 針對欄位1作升冪<br>$orderby= Field1 asc</br> |
| orderby{Field desc} | 針對某欄位作降冪 | 針對欄位1作降冪<br>$orderby= Field1 desc</br>|






###  更多OData服務開發教學請詳見[連結](http://ptx.transportdata.tw/ptx/Download/公共運輸整合資訊平台資料服務開發實作.pdf)。
