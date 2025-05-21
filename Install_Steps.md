#### ▶ 安裝 Python (3.12.4)
- 下載並安裝 [Python 3.12.4](https://www.python.org/downloads/)  
- 勾選「Add Python to PATH」(就無需另外加入系統環境變數)

---

#### ▶ 安裝 PostgreSQL (14.17)
- 安裝 [PostgreSQL 14.17](https://www.postgresql.org/download/)  
- 設定資料庫密碼  
- 設定埠號

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
- 新增 `odoo.conf`，內容範例：

```ini
[options]
db_user = 自訂
db_password = 自訂
addons_path = C:/odoo-18.0/addons
logfile = C:/odoo-18.0/logs/odoo.log
```

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
- 執行以下指令可啟動伺服器：

```bash
cd C:\odoo-18.0
python odoo-bin -c odoo.conf
```

- 可將下列內容存成 `start_odoo.bat`，雙擊即可啟動伺服器：

```bat
@echo off
cd /d C:\odoo-18.0
python odoo-bin -c odoo.conf
pause
```

---

#### :star: 安裝 wkhtmltopdf（PDF 生成功能）
- 前往 [wkhtmltopdf 0.12.5 下載頁](https://github.com/wkhtmltopdf/wkhtmltopdf/releases/0.12.5/)  
- 下載並安裝 `wkhtmltox-0.12.5-1.msvc2015-win64.exe`  
- 將路徑 `C:\Program Files\wkhtmltopdf\bin` 加入系統環境變數

---

### 🔶 離線安裝

#### 🔻 線上環境準備
- 下載以下安裝檔：
   - [Python 安裝檔](https://www.python.org/downloads/)
   - [PostgreSQL 安裝檔](https://www.postgresql.org/download/)
   - Odoo 壓縮檔（從 Odoo 官網或 GitHub 取得）

- 安裝 Python 後，使用 `requirements.txt` 下載 Odoo 所需套件：
   - 先將 Odoo 壓縮檔解壓縮，找到 `requirements.txt`
   - 執行以下指令安裝 pip 套件至指定資料夾：

```bat
mkdir odoo_packages
pip download -r requirements.txt -d odoo_packages
```

- 將以下資料複製到離線環境
   - Python 安裝檔
   - PostgreSQL 安裝檔
   - Odoo 壓縮檔
   - odoo_packages 資料夾

#### 🔻 離線環境安裝
- 安裝 Python 與 PostgreSQL，並記得加入系統環境變數
- 解壓縮 Odoo 壓縮檔
- 執行以下指令安裝 Odoo 所需套件：

```bat
pip install --no-index --find-links=odoo_packages -r requirements.txt
```

- 完成上述安裝後，其餘步驟與有網路環境相同，可依正常流程啟動 Odoo



