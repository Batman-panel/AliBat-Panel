[README (2).md](https://github.com/user-attachments/files/33017742/README.2.md)
# AliBat Panel - Premium VPN Management

<div align="center">

![Version](https://img.shields.io/badge/version-2.0.0-red)
![Node](https://img.shields.io/badge/node-%3E%3D18-green)
![License](https://img.shields.io/badge/license-MIT-blue)
![Katabump](https://img.shields.io/badge/Katabump-Compatible-orange)

**پنل مدیریت VPN حرفه‌ای | Professional VPN Management Panel**

[فارسی](#-راهنمای-فارسی) | [English](#-english-guide)

</div>

---

## 🌟 ویژگی‌ها | Features

### 🇮 فارسی
- ✅ **۹ پروتکل پشتیبانی**: Hysteria2, VLESS-WS, VLESS-gRPC, Trojan-WS, Shadowsocks, WireGuard, TUIC, XHTTP, Cloudflare Argo
-  **رابط کاربری زیبا**: تم قرمز-طلایی با طراحی مدرن
- 📊 **مانیتورینگ زنده**: CPU, RAM, آمار کاربران به صورت لحظه‌ای
- 🛡️ **وایرگارد کامل**: تولید خودکار کانفیگ برای هر کاربر
- ⚡ **تست سرعت**: تست دانلود/آپلود/پینگ داخلی
- 💾 **بکاپ‌گیری**: دانلود و بازیابی کامل اطلاعات
- 🔐 **امنیت بالا**: رمزنگاری scrypt، محدودیت اتصال، حجم و انقضا
-  **بدون محدودیت زمانی**: دور زدن محدودیت‌های Katabump با GitHub Actions

### 🇬🇧 English
- ✅ **9 Protocols**: Hysteria2, VLESS-WS, VLESS-gRPC, Trojan-WS, Shadowsocks, WireGuard, TUIC, XHTTP, Cloudflare Argo
-  **Beautiful UI**: Red-gold theme with modern design
- 📊 **Live Monitoring**: CPU, RAM, user stats in real-time
- ️ **Full WireGuard**: Auto-generate config for each user
- ⚡ **Speed Test**: Built-in download/upload/ping test
- 💾 **Backup System**: Full data download and restore
- 🔐 **High Security**: scrypt encryption, connection limits, volume & expiry
-  **No Time Limits**: Bypass Katabump restrictions with GitHub Actions

---

##  اسکرین‌شات | Screenshots
<img width="1903" height="944" alt="image" src="https://github.com/user-attachments/assets/70d71d6b-588c-4f88-b821-1499d6b894c3" />
<img width="1920" height="943" alt="image" src="https://github.com/user-attachments/assets/7b283910-1387-4a2d-9bf2-fcbd30cac9d4" />

<div align="center">

![Dashboard](https://img.shields.io/badge/Dashboard-داشبورد-red)
![Users](https://img.shields.io/badge/Users-کاربران-gold)
![WireGuard](https://img.shields.io/badge/WireGuard-وایرگارد-blue)
![SpeedTest](https://img.shields.io/badge/Speed%20Test-تست%20سرعت-green)
<img width="1905" height="932" alt="image" src="https://github.com/user-attachments/assets/730fa68a-adc1-4a15-a2fb-6494e389a2f9" />
<img width="1903" height="933" alt="image" src="https://github.com/user-attachments/assets/96059570-c867-4ec2-9b6f-de69bfc9aee0" />

</div>

---

# 🇮 راهنمای فارسی

## 🚀 نصب روی Katabump

### مرحله : ساخت پروژه در Katabump

1. وارد [Katabump](https://control.katabump.com) شوید
2. روی **Create Server** کلیک کنید
3. **Node.js** را انتخاب کنید
4. نام سرور را وارد کنید (مثلاً: `AliBat Panel`)

### مرحله ۲: آپلود فایل‌ها

دو فایل زیر را در ریشه پروژه آپلود کنید:

#### 📄 `package.json`

```json
{
  "name": "alibat-panel",
  "version": "2.0.0",
  "description": "AliBat Panel - Secure Multi-Protocol VPN Management Panel",
  "main": "index.js",
  "scripts": {
    "start": "node index.js"
  },
  "dependencies": {
    "express": "^4.21.0"
  },
  "engines": {
    "node": ">=18"
  },
  "author": "AliBat Panel",
  "license": "MIT"
}
```

#### 📄 `index.js`

فایل `index.js` را از ریپازیتوری دانلود کنید (۷۰+ خط کد کامل).

### مرحله : نصب و اجرا

در کنسول Katabump دستورات زیر را بزنید:

```bash
# نصب وابستگی‌ها
npm install

# اجرای پنل
npm start
```

### مرحله ۴: دسترسی به پنل

1. بعد از اجرا، URL سرور را کپی کنید
2. در مرورگر باز کنید
3. **اولین ورود**: صفحه تنظیم رمز نمایش داده می‌شود
4. رمز دلخواه (حداقل ۸ کاراکتر) وارد کنید
5. وارد داشبورد شوید! 🎉

---

## 🔓 دور زدن محدودیت زمانی Katabump

### مشکل چیست؟

Katabump سرورهای رایگان را هر چند روز یکبار **غیرفعال** می‌کند و باید دکمه **Renew** را بزنید. این اسکریپت این کار را **خودکار** انجام می‌دهد!

### روش کار

ما از **GitHub Actions** + **Playwright** استفاده می‌کنیم تا هر ۳ روز یکبار خودکار وارد Katabump شود و دکمه Renew را بزند.

### مرحله ۱: ساخت ریپازیتوری GitHub

1. وارد [GitHub](https://github.com) شوید
2. یک ریپازیتوری جدید بسازید (مثلاً: `katabump-renew`)
3. ریپازیتوری را **Private** کنید (چون رمز عبور دارید)

### مرحله : آپلود فایل‌های تمدید

دو فایل زیر را در ریپازیتوری آپلود کنید:

#### 📄 `renew.py`

```python
import os
import time
from playwright.sync_api import sync_playwright

EMAIL = os.environ.get("KATABUMP_EMAIL")
PASSWORD = os.environ.get("KATABUMP_PASSWORD")
SERVER_ID = os.environ.get("SERVER_ID", "d1712508")

def main():
    if not EMAIL or not PASSWORD:
        print("❌ خطا: متغیرهای KATABUMP_EMAIL یا KATABUMP_PASSWORD در Secrets تعریف نشده‌اند.")
        return

    with sync_playwright() as p:
        browser = p.chromium.launch(headless=True)
        context = browser.new_context(
            user_agent="Mozilla/5.0 (Windows NT 10.0; Win64; x64) AppleWebKit/537.36 (KHTML, like Gecko) Chrome/122.0.0.0 Safari/537.36",
            viewport={"width": 1280, "height": 720}
        )
        page = context.new_page()

        try:
            print(" در حال ورود به صفحه لاگین Katabump...")
            page.goto("https://control.katabump.com/auth/login", wait_until="domcontentloaded", timeout=60000)
            page.wait_for_timeout(6000)

            print("🔑 در حال وارد کردن اطلاعات لاگین...")
            user_input = page.locator('input[name="username"], input[name="email"], input[type="text"], input[type="email"]').first
            pass_input = page.locator('input[name="password"], input[type="password"]').first

            user_input.fill(EMAIL)
            pass_input.fill(PASSWORD)

            submit_btn = page.locator('button[type="submit"], input[type="submit"]').first
            submit_btn.click()

            page.wait_for_timeout(8000)

            print(f" در حال هدایت به سرور {SERVER_ID}...")
            page.goto(f"https://control.katabump.com/server/{SERVER_ID}", wait_until="domcontentloaded", timeout=60000)
            page.wait_for_timeout(6000)

            renew_btn = page.locator('button:has-text("Renew"), a:has-text("Renew")')
            if renew_btn.count() > 0 and renew_btn.first.is_visible():
                renew_btn.first.click()
                print("🎉 دکمه Renew با موفقیت کلیک شد!")
                page.wait_for_timeout(3000)
            else:
                print("ℹ️ دکمه Renew در حال حاضر فعال نیست یا سرور نیازی به تمدید ندارد.")

        except Exception as e:
            print(f"❌ خطایی رخ داد: {e}")
            page.screenshot(path="error_screenshot.png")
            raise e
        finally:
            browser.close()

if __name__ == "__main__":
    main()
```

#### 📄 `.github/workflows/renew.yml`

```yaml
name: Katabump Auto Renew

on:
  schedule:
    # اجرای خودکار هر ۳ روز یک‌بار
    - cron: '0 12 */3 * *'
  workflow_dispatch: # امکان اجرای دستی برای تست فوری

jobs:
  renew-job:
    runs-on: ubuntu-latest

    steps:
      - name: دریافت کدها
        uses: actions/checkout@v4

      - name: نصب پایتون
        uses: actions/setup-python@v4
        with:
          python-version: '3.10'

      - name: نصب ابزارها و مرورگر
        run: |
          python -m pip install --upgrade pip
          pip install playwright
          playwright install chromium
          playwright install-deps

      - name: اجرای اسکریپت تمدید
        env:
          KATABUMP_EMAIL: ${{ secrets.KATABUMP_EMAIL }}
          KATABUMP_PASSWORD: ${{ secrets.KATABUMP_PASSWORD }}
          SERVER_ID: ${{ secrets.SERVER_ID }}
        run: python renew.py
```

### مرحله ۳: تنظیم Secrets در GitHub

1. در ریپازیتوری GitHub، به **Settings** بروید
2. از منوی سمت چپ، **Secrets and variables** → **Actions** را انتخاب کنید
3. روی **New repository secret** کلیک کنید
4. این ۳ Secret را اضافه کنید:

| Secret Name | مقدار | توضیح |
|-------------|--------|--------|
| `KATABUMP_EMAIL` | ایمیل اکانت Katabump | ایمیلی که با آن ثبت‌نام کردید |
| `KATABUMP_PASSWORD` | رمز عبور Katabump | رمز اکانت Katabump |
| `SERVER_ID` | آیدی سرور | از URL سرور کپی کنید (مثلاً: `d1712508`) |

### مرحله ۴: پیدا کردن SERVER_ID

1. وارد Katabump شوید
2. به صفحه سرور خود بروید
3. در URL، عدد بعد از `/server/` را کپی کنید:
   ```
   https://control.katabump.com/server/d1712508
                                            ^^^^^^^^
                                            این را کپی کنید
   ```

### مرحله ۵: تست دستی

1. در ریپازیتوری GitHub، به تب **Actions** بروید
2. روی **Katabump Auto Renew** کلیک کنید
3. دکمه **Run workflow** را بزنید
4. منتظر بمانید تا اجرا شود (-۳ دقیقه)
5. اگر موفقیت‌آمیز بود، ✅ سبز می‌بینید

### مرحله ۶: زمان‌بندی خودکار

اسکریپت هر **۳ روز یکبار** ساعت ۱۲:۰۰ UTC خودکار اجرا می‌شود.

اگر می‌خواهید زمان را تغییر دهید، در فایل `renew.yml` این خط را ویرایش کنید:

```yaml
- cron: '0 12 */3 * *'  # هر ۳ روز
# یا
- cron: '0 12 */2 * *'  # هر  روز
# یا
- cron: '0 12 * * *'    # هر روز
```

---

## ⚙️ تنظیمات پیشرفته

### تغییر پورت

اگر می‌خواهید پورت پنل را تغییر دهید، در فایل `index.js` این خط را پیدا کنید:

```javascript
const PORT = process.env.PORT || 3000;
```

و عدد `3000` را به پورت دلخواه تغییر دهید.

### فعال/غیرفعال کردن پروتکل‌ها

بعد از ورود به پنل، به بخش **تنظیمات** بروید و پروتکل‌های مورد نظر را فعال/غیرفعال کنید.

### بکاپ‌گیری

1. در پنل، به **تنظیمات** → **بکاپ** بروید
2. روی **دانلود بکاپ** کلیک کنید
3. فایل JSON ذخیره می‌شود
4. برای بازیابی، روی **بازیابی** کلیک و فایل را انتخاب کنید

---

## 🛠️ عیب‌یابی

### ❌ خطا: `Cannot find module 'express'`

**راه حل**: دستور `npm install` را بزنید.

###  خطا: `PORT already in use`

**راه حل**: پورت دیگری در `index.js` انتخاب کنید یا از environment variable استفاده کنید.

### ❌ خطا: `Setup already completed`

**راه حل**: فایل `data/store.json` را حذف کنید و دوباره `npm start` بزنید.

### ❌ اسکریپت Renew کار نمی‌کند

**راه حل**:
1. Secrets را در GitHub چک کنید
2. SERVER_ID را بررسی کنید
3. در GitHub Actions، لاگ اجرا را ببینید
4. اگر خطا داشت، screenshot در ریپازیتوری ذخیره می‌شود

---

# 🇬🇧 English Guide

## 🚀 Installation on Katabump

### Step 1: Create Project in Katabump

1. Login to [Katabump](https://control.katabump.com)
2. Click **Create Server**
3. Select **Node.js**
4. Enter server name (e.g., `AliBat Panel`)

### Step 2: Upload Files

Upload these two files to the project root:

#### 📄 `package.json`

```json
{
  "name": "alibat-panel",
  "version": "2.0.0",
  "description": "AliBat Panel - Secure Multi-Protocol VPN Management Panel",
  "main": "index.js",
  "scripts": {
    "start": "node index.js"
  },
  "dependencies": {
    "express": "^4.21.0"
  },
  "engines": {
    "node": ">=18"
  },
  "author": "AliBat Panel",
  "license": "MIT"
}
```

#### 📄 `index.js`

Download `index.js` from the repository (700+ lines of complete code).

### Step 3: Install and Run

In Katabump console, run:

```bash
# Install dependencies
npm install

# Start the panel
npm start
```

### Step 4: Access the Panel

1. After running, copy the server URL
2. Open in browser
3. **First login**: Setup password page appears
4. Enter your password (minimum 8 characters)
5. Enter the dashboard! 🎉

---

## 🔓 Bypassing Katabump Time Limits

### What's the Problem?

Katabump **disables** free servers every few days and you must click the **Renew** button. This script does it **automatically**!

### How It Works

We use **GitHub Actions** + **Playwright** to automatically login to Katabump every 3 days and click the Renew button.

### Step 1: Create GitHub Repository

1. Login to [GitHub](https://github.com)
2. Create a new repository (e.g., `katabump-renew`)
3. Make it **Private** (because it contains passwords)

### Step 2: Upload Renewal Files

Upload these two files to the repository:

####  `renew.py`

```python
import os
import time
from playwright.sync_api import sync_playwright

EMAIL = os.environ.get("KATABUMP_EMAIL")
PASSWORD = os.environ.get("KATABUMP_PASSWORD")
SERVER_ID = os.environ.get("SERVER_ID", "d1712508")

def main():
    if not EMAIL or not PASSWORD:
        print("❌ Error: KATABUMP_EMAIL or KATABUMP_PASSWORD secrets not defined.")
        return

    with sync_playwright() as p:
        browser = p.chromium.launch(headless=True)
        context = browser.new_context(
            user_agent="Mozilla/5.0 (Windows NT 10.0; Win64; x64) AppleWebKit/537.36 (KHTML, like Gecko) Chrome/122.0.0.0 Safari/537.36",
            viewport={"width": 1280, "height": 720}
        )
        page = context.new_page()

        try:
            print("🔄 Logging into Katabump...")
            page.goto("https://control.katabump.com/auth/login", wait_until="domcontentloaded", timeout=60000)
            page.wait_for_timeout(6000)

            print("🔑 Entering login credentials...")
            user_input = page.locator('input[name="username"], input[name="email"], input[type="text"], input[type="email"]').first
            pass_input = page.locator('input[name="password"], input[type="password"]').first

            user_input.fill(EMAIL)
            pass_input.fill(PASSWORD)

            submit_btn = page.locator('button[type="submit"], input[type="submit"]').first
            submit_btn.click()

            page.wait_for_timeout(8000)

            print(f"🌐 Navigating to server {SERVER_ID}...")
            page.goto(f"https://control.katabump.com/server/{SERVER_ID}", wait_until="domcontentloaded", timeout=60000)
            page.wait_for_timeout(6000)

            renew_btn = page.locator('button:has-text("Renew"), a:has-text("Renew")')
            if renew_btn.count() > 0 and renew_btn.first.is_visible():
                renew_btn.first.click()
                print("🎉 Renew button clicked successfully!")
                page.wait_for_timeout(3000)
            else:
                print("ℹ️ Renew button is not active or server doesn't need renewal.")

        except Exception as e:
            print(f"❌ Error occurred: {e}")
            page.screenshot(path="error_screenshot.png")
            raise e
        finally:
            browser.close()

if __name__ == "__main__":
    main()
```

#### 📄 `.github/workflows/renew.yml`

```yaml
name: Katabump Auto Renew

on:
  schedule:
    # Auto-run every 3 days
    - cron: '0 12 */3 * *'
  workflow_dispatch: # Manual trigger for testing

jobs:
  renew-job:
    runs-on: ubuntu-latest

    steps:
      - name: Checkout code
        uses: actions/checkout@v4

      - name: Setup Python
        uses: actions/setup-python@v4
        with:
          python-version: '3.10'

      - name: Install tools and browser
        run: |
          python -m pip install --upgrade pip
          pip install playwright
          playwright install chromium
          playwright install-deps

      - name: Run renewal script
        env:
          KATABUMP_EMAIL: ${{ secrets.KATABUMP_EMAIL }}
          KATABUMP_PASSWORD: ${{ secrets.KATABUMP_PASSWORD }}
          SERVER_ID: ${{ secrets.SERVER_ID }}
        run: python renew.py
```

### Step 3: Configure GitHub Secrets

1. In your GitHub repository, go to **Settings**
2. From left menu, select **Secrets and variables** → **Actions**
3. Click **New repository secret**
4. Add these 3 secrets:

| Secret Name | Value | Description |
|-------------|--------|-------------|
| `KATABUMP_EMAIL` | Your Katabump email | Email you registered with |
| `KATABUMP_PASSWORD` | Your Katabump password | Your account password |
| `SERVER_ID` | Server ID | Copy from server URL (e.g., `d1712508`) |

### Step 4: Find SERVER_ID

1. Login to Katabump
2. Go to your server page
3. In the URL, copy the number after `/server/`:
   ```
   https://control.katabump.com/server/d1712508
                                            ^^^^^^^^
                                            Copy this
   ```

### Step 5: Manual Test

1. In GitHub repository, go to **Actions** tab
2. Click **Katabump Auto Renew**
3. Click **Run workflow**
4. Wait for it to complete (2-3 minutes)
5. If successful, you'll see ✅ green checkmark

### Step 6: Automatic Scheduling

The script runs automatically every **3 days** at 12:00 UTC.

To change the schedule, edit this line in `renew.yml`:

```yaml
- cron: '0 12 */3 * *'  # Every 3 days
# or
- cron: '0 12 */2 * *'  # Every 2 days
# or
- cron: '0 12 * * *'    # Every day
```

---

## ⚙️ Advanced Configuration

### Change Port

To change the panel port, find this line in `index.js`:

```javascript
const PORT = process.env.PORT || 3000;
```

And change `3000` to your desired port.

### Enable/Disable Protocols

After logging into the panel, go to **Settings** and enable/disable protocols as needed.

### Backup

1. In the panel, go to **Settings** → **Backup**
2. Click **Download Backup**
3. JSON file will be saved
4. To restore, click **Restore** and select the file

---

## ️ Troubleshooting

### ❌ Error: `Cannot find module 'express'`

**Solution**: Run `npm install`.

### ❌ Error: `PORT already in use`

**Solution**: Choose a different port in `index.js` or use environment variable.

### ❌ Error: `Setup already completed`

**Solution**: Delete `data/store.json` file and run `npm start` again.

### ❌ Renew script not working

**Solution**:
1. Check GitHub secrets
2. Verify SERVER_ID
3. View execution logs in GitHub Actions
4. If error, screenshot is saved in repository

---

## 📊 Architecture

```
AliBat Panel
├── Frontend (HTML/CSS/JS inline)
├── Backend (Node.js + Express)
├── Data Store (JSON file)
└── Auto Renew (GitHub Actions + Playwright)
```

---

## 🔐 Security Features

- ✅ **Password Hashing**: scrypt with salt
- ✅ **Session Management**: Auto-expire after 7 days
- ✅ **Rate Limiting**: Login attempts limited
- ✅ **User Isolation**: Separate UUID and keys per user
- ✅ **Connection Limits**: Max connections per user
- ✅ **Volume Control**: Enforced data limits
- ✅ **Expiry Dates**: Automatic account expiration

---

##  Supported Protocols

| Protocol | Port | Description |
|----------|------|-------------|
| Hysteria2 | Main | QUIC-based, ultra-fast |
| VLESS-WS | Main | WebSocket, compatible |
| VLESS-gRPC | Main | gRPC, Cloudflare-friendly |
| Trojan-WS | Main | Trojan over WebSocket |
| Shadowsocks | Main | AES-256-GCM encryption |
| WireGuard | Main | Modern VPN, fastest |
| TUIC | 8443 | QUIC-based, low latency |
| XHTTP | Main | Latest protocol |
| Argo | 443 | Cloudflare tunnel |

---

## 📝 License

MIT License - See LICENSE file for details

---

##  Contribution

Contributions welcome! Please fork the repository and submit a pull request.

---

## 📞 Support

- 📱 Telegram 1: [@BATMAN_Pane_L](https://t.me/BATMAN_Pane_L)
- 📱 Telegram 2: [@alibodama](https://t.me/alibodama)
- 📺 YouTube 1: [@Batman-V-P-N](https://www.youtube.com/@Batman-V-P-N)
- 📺 YouTube 2: [@alibodama](https://www.youtube.com/@alibodama)

---

## ⭐ Star History

If you find this project useful, please give it a star! ⭐

---

<div align="center">

**Made with ❤️ by AliBat Panel Team**

[⬆️ Back to Top](#-alibat-panel---premium-vpn-management)

</div>
