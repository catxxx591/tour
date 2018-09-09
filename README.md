Tour
==

##使用requests建立orange()和gloria()兩方法爬取澄果旅遊和華泰旅遊資料，存入mysql資料庫
 

- 使用datetime.now()套進payload，post當日最新資料

- 用bs4選取當日網站總頁數，並依序爬取資料

- 參考旅遊咖網站資料，做table的規劃
        - 用sqlalchemy在mtsql新增table，再用pd.to_sql() append資料
        
- 定義update_table()方法，更新日後爬取的新資料
        -先判斷主鍵是否已存在table中，如果不存在就insert新資料
        -insert完畢後依iterrow()完成資料update