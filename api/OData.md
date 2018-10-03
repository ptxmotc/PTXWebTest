## 【支援OData查詢語法】



###  OData語法

| OData語法 |  說明  | 範例  |
| :--: | :--------: | :--------: |
| format | 資料格式json、xml、csv | 回傳xml格式<br>$format=xml</br> |
| select | 回傳資料的某些欄位 | 回傳欄位1<br>$select= Field1</br>|
| top | 取最前筆數 | 取前10筆 <br>$top=10</br> |
| skip | 跳過筆數 | 跳過前100筆 <br>$skip=100</br> |
| filter | 回傳符合特定表達式的資料 | 車牌號碼等於636-U7的資料<br>$filter=PlateNumb eq '636-U7'</br> |
| date | 日期 | UpdateTime的日期格式為2015-09-17的資料<br>$filter=date(UpdateTime) eq  2015-09-17</br>  |
| time | 時間 | UpdateTime的時間格式為17:57:00+08:00的資料<br>$filter=time(UpdateTime) eq 11:59:48</br> |
| contains | 包含 | 車牌號碼包含FA的資料<br>$filter=contains(PlateNumb, 'FA')</br> |
| all | 所有項目都要符合|針對停靠時間資料底下車站代碼，全部的車站代碼為1000的資料就回傳 <br> $filter=StopTimes/all(d:d/StationID eq '1000')</br> |
| any | 其中一項符合 | 針對停靠時間資料底下車站代碼，任一筆的車站代碼為1000的資料就回傳 <br>$filter=StopTimes/any(d:d/StationID eq  '1000')</br> |
| orderby {Field asc} | 針對某欄位作升冪 | 針對欄位1作升冪<br>$orderby= Field1 asc</br> |
| orderby{Field desc} | 針對某欄位作降冪 | 針對欄位1作降冪<br>$orderby= Field1 desc</br>|
| spatialFilter | 尋找附近點位資料 | 尋找中心點: 緯度25.05463, 經度121.46584 ，範圍150 公尺內的資料<br>$spatialFilter=nearby(StopPosition, 25.05463, 121.46584, 150) </br>|







###  更多OData服務開發教學請詳見以下連結
   [http://ptx.transportdata.tw/ptx/Download/公共運輸整合資訊平台資料服務開發實作.pdf](https://docs.google.com/viewer?url=https://github.com/ptxmotc/PTX_Web/blob/master/Swagger%E6%9C%8D%E5%8B%99%E8%AA%AA%E6%98%8E%E4%B8%8A%E5%82%B3%E5%8F%83%E8%80%83%E6%AA%94%E6%A1%88/%E5%85%AC%E5%85%B1%E9%81%8B%E8%BC%B8%E6%95%B4%E5%90%88%E8%B3%87%E8%A8%8A%E5%B9%B3%E5%8F%B0%E8%B3%87%E6%96%99%E6%9C%8D%E5%8B%99%E9%96%8B%E7%99%BC%E5%AF%A6%E4%BD%9C.pdf?raw=true)
