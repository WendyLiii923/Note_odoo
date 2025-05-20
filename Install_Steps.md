## 安裝 Python (3.12.4) ##
下載並安裝 Python，並確保選擇「Add Python to PATH」選項。  

## 安裝 PostgreSQL (14.17) ##
安裝 PostgreSQL，設置資料庫密碼並確保它正在運行。  
- 設定Server密碼  
- 設置Port 5432  

## 安裝 odoo (18) ##
解壓 odoo 18 的 ZIP 文件到你選擇的目錄。   

## 安裝 相關套件 ##
用cmd執行下方指令來安裝套件
cd odoo-18.0 
pip install -r requirements.txt

## 新增 odoo 配置文件 ##
創建 odoo 配置文件 odoo.conf，並設置資料庫連接（包括 PostgreSQL 伺服器的用戶名、密碼和資料庫名）。 

## 啟動 Odoo 伺服器 ##
在命令提示符中執行 python odoo-bin 啟動 Odoo。 (可以寫成.bat)  
cd C:/odoo  
python odoo-bin -c odoo.conf -d odoo -i base  
python odoo-bin -c odoo.conf  


*****
## 加裝wkhtmltopdf ##
https://github.com/wkhtmltopdf/wkhtmltopdf/releases/0.12.5/  
下載wkhtmltox-0.12.5-1.msvc2015-win64.exe  
安裝後，加入環境變數 C:\Program Files\wkhtmltopdf\bin
