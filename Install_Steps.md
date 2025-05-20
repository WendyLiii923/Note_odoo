#### ▶ 安裝 Python (3.12.4)
- 下載並安裝 [Python 3.12.4](https://www.python.org/downloads/)  
- 勾選「Add Python to PATH」(就無需另外加入系統環境變數)

---

#### ▶ 安裝 PostgreSQL (14.17)
- 安裝 [PostgreSQL 14.17](https://www.postgresql.org/download/)  
- 設定資料庫密碼  
- 確認埠號為 `5432`  
- 確認服務正常啟動

---

#### ▶ 安裝 Odoo (18)
- 解壓 Odoo 18 ZIP 檔至任意目錄，例如：`C:\odoo-18.0`

---

#### ▶ 安裝相關套件
- 執行以下指令安裝相關套件

   ```bash
   cd C:\odoo-18.0
   pip install -r requirements.txt
   ```

---

#### ▶ 建立 Odoo 設定檔
- 新增 `odoo.conf`，設定內容包含：  
   - PostgreSQL 使用者帳號  
   - 密碼  
   - 資料庫名稱  

---

#### ▶ 初始化資料庫（首次建立 DB 時執行）
如果是第一次執行，且需要初始化安裝模組，可執行以下指令：

```bash
cd C:\odoo-18.0
python odoo-bin -c odoo.conf -d odoo -i base
```
> ※ 僅需在首次建立資料庫或需要重新安裝模組時使用 `-i`（install）選項

---

#### ▶ 啟動 Odoo 伺服器
執行以下指令可啟動 Odoo：

```bash
cd C:\odoo-18.0
python odoo-bin -c odoo.conf
```

---

#### ▶ 建立啟動用 .bat 檔
可將下列內容存成 `start_odoo.bat`，雙擊即可啟動 Odoo：

```bat
@echo off
cd /d C:\odoo-18.0
python odoo-bin -c odoo.conf
pause
```

---

#### ▶ 安裝 wkhtmltopdf（PDF 生成功能）
- 前往 [wkhtmltopdf 0.12.5 下載頁](https://github.com/wkhtmltopdf/wkhtmltopdf/releases/0.12.5/)  
- 下載並安裝 `wkhtmltox-0.12.5-1.msvc2015-win64.exe`  
- 將路徑 `C:\Program Files\wkhtmltopdf\bin` 加入系統環境變數
