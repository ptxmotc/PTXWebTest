# 所有公共運輸資料資料檢核項目

(一)	完整性檢核


### 1.	必填欄位不可為空值&#xD;

(1)	檢核欄位：必填欄位

(2)	說明：

設定為必填的欄位內容正常不可為空值，若為空值表示異常。

(3)	範例：

公車站牌資料Stop XML之StopID機關定義站牌代號、StopName站牌名稱等必填欄位欄位內容不可為空值。

(4)	檢核方式：XSD檢核

(5)	建議檢核頻率：每月

### 2.	選填欄位部分空值&#xD;

(1)	檢核欄位：選填欄位

(2)	說明：

設定為選填的欄位內容部分有值，部分為空值，此為正常情形，但可針對此發出告警。

(3)	範例：

公車附屬路線資料SubRoute XML之HeadSign車頭文字描述，該欄位內容部分有描述，部分為空值，雖然不屬於異常但可以對此發出告警，請來源單位補齊資料。

(4)	檢核方式：XSD檢核

(5)	建議檢核頻率：每月

(二)	重複性檢核


### 1.	資料主代碼重複&#xD;

(1)	檢核欄位：代碼欄位

(2)	說明：

各資料ID代碼比對是否有重複的資料。

(3)	範例：

公車站牌資料Stop XML之StopID機關定義站牌代號是否有重複。

(4)	檢核方式：XSD檢核

(5)	建議檢核頻率：每月

(三)	合理性檢核


### 1.	空格排除&#xD;

(1)	檢核欄位：非空值欄位

(2)	說明：

欄位內容不可包含空格

(3)	範例：

公車站牌資料Stop XML之StopName站牌名稱欄位不可包含空格。

(4)	檢核方式：XSD檢核

(5)	建議檢核頻率：每月

### 2.	特殊字元排除與全形半形轉換&#xD;

(1)	檢核欄位：非空值欄位

(2)	說明：

欄位內容不可包含特殊字元，例如：「\」和「\*」，或是全形和半形文字參雜，需轉換為一致樣式

(3)	範例：

台鐵定期車次時刻表資料GeneralTrainTimeTable XML之Note附註說明欄位不可全形和半形文字參雜。

(4)	檢核方式：XSD檢核

(5)	建議檢核頻率：每月

(四)	格式檢核


### 1.	時間格式&#xD;

(1)	檢核欄位：日期時間欄位

(2)	說明：

紀錄日期或時間之欄位是否符合ISO8601格式(yyyy-MM-ddTHH:mm:sszzz)

(3)	範例：

公車最新消息資料News XML之UpdateTime更新日期時間、PublishTime消息公告日期時間、StartTime開始日期時間、EndTime結束日期時間。

(4)	檢核方式：XSD檢核

(5)	建議檢核頻率：每月

(五)	值域檢核


### 1.	資料為特定類別數值&#xD;

(1)	檢核欄位：

Direction方向性描述、HasSubRoutes是否有附屬路線、ServiceStatus營運服務狀態代碼、TicketType票種類型……等

(2)	說明：

類別資料是否為特定數值。

(3)	範例：

公車路線站序資料StopOfRoute XML之Direction方向性描述，該欄位的數值是否為0(去程)、1(返程)或2(迴圈)。

(4)	檢核方式：XSD檢核

(5)	建議檢核頻率：每月



 

