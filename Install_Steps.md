安裝 Python 3.12.4：  
下載並安裝 Python，並確保選擇「Add Python to PATH」選項。  

安裝 PostgreSQL 14.17：  
安裝 PostgreSQL，設置資料庫密碼並確保它正在運行。  
設定Server密碼  
設置Port 5432  

安裝 Odoo 18：  
解壓 Odoo 18 的 ZIP 文件到你選擇的目錄。  

設置 Odoo 配置文件：  
創建 Odoo 配置文件 odoo.conf，並設置資料庫連接（包括 PostgreSQL 伺服器的用戶名、密碼和資料庫名）。  

安裝 相關套件  

啟動 Odoo 伺服器：  
在命令提示符中執行 python odoo-bin 啟動 Odoo。  
cd C:/odoo  
python odoo-bin -c odoo.conf -d odoo -i base  
python odoo-bin -c odoo.conf  
