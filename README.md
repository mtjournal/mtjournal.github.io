# MT4 Journal — MetaTrader 4 Trading Journal

A free, fully offline Windows app that **automatically** logs your MetaTrader 4 trades and shows your real performance with stats, charts and strategy management.

> Website: **https://mtjournal.github.io** — The app's source lives in a separate repo; this repo hosts the landing page and releases.

![Version](https://img.shields.io/badge/version-0.23.2-blue) ![Platform](https://img.shields.io/badge/platform-Windows%20x64%20%7C%20ARM64-lightgrey) ![License](https://img.shields.io/badge/license-MIT-green)

`English` · [فارسی](#فارسی)

---

## English

### 📥 Download & Install

1. Head to the [**Releases**](https://github.com/mtjournal/mtjournal.github.io/releases) page and grab the latest version.
2. Pick the file that matches your system:

| File | Target |
|---|---|
| `MT4 Journal-Setup-x64-<version>.exe` | Windows 64-bit (recommended — most PCs) |
| `MT4 Journal-Setup-arm64-<version>.exe` | Windows on ARM devices |
| `MT4 Journal-Setup-<version>.exe` | Combined (both architectures) |

3. Run the installer, choose the install folder and you're done. No extra prerequisites required.

### 🚀 Setup — Connect to MetaTrader Automatically

After installing, do this **once**; everything is automatic from then on:

1. Run the app. On first launch, enter the path to your MetaTrader `terminal.exe` (or browse for it).
2. Click **Auto-install EA in MetaTrader** — the app copies and compiles the `Mt4JournalExporter` expert into your MT4 folder for you.
3. In MT4, drag the `Mt4JournalExporter` expert from *Navigator → Expert Advisors* onto any chart.
4. In the *Account History* tab, right-click → **All History** so your full history gets imported.
5. Done! ✅ Every closed trade lands in the journal automatically within seconds.

**How does it work?** The EA writes every closed trade to a CSV file inside the MT4 folder; the app reads it every few seconds and stores it in a local SQLite database. Your data (notes, rewards, strategies, screenshots) is preserved on re-sync, and nothing is ever uploaded anywhere.

#### Alternative — without the EA

If you'd rather not use the EA: in MT4, right-click *Account History* → **All History** → **Save as Report**, then use **Import HTML Report** in the app.

#### If the MT4 folder isn't found

Open the app's **Settings** and paste the path of the folder that contains `MQL4` — usually:

```
%APPDATA%\MetaQuotes\Terminal\<TERMINAL_HASH>
```

### 🛠 Daily Use

- **Nothing to do** — trades are logged automatically.
- Click any trade to add **notes** (entry reason, mistakes, lessons), assign a **reward** and attach **chart screenshots**.
- **Define your strategies** and assign them to trades; the trades table and stats filter by strategy.
- In the **Stats** screen, see net P/L, win rate, profit factor, the monthly trading calendar and daily / monthly / symbol / equity-curve charts.
- Dates are shown in the **Jalali (Solar Hijri) calendar** with Iran time (Gregorian mode also available).
- Switch between **multiple accounts** from the toolbar and toggle the UI language (English/Persian).

### 🔒 Privacy

The database and images are stored locally next to the app only. The app doesn't need internet and never sends any data to any server.

---

## فارسی

[English ↑](#english) · `فارسی`

برنامه‌ای رایگان و کاملاً آفلاین برای ویندوز که معاملات متاتریدر ۴ را **به‌صورت خودکار** ثبت می‌کند و به‌همراه آمار، نمودار و مدیریت استراتژی، عملکرد واقعی‌ات را نشان می‌دهد.

> لینک سایت: **https://mtjournal.github.io** — سورس برنامه در ریپوی جداگانه است؛ این ریپو فقط سایت معرفی و ریلیزهاست.

### 📥 دانلود و نصب

1. به بخش [**Releases**](https://github.com/mtjournal/mtjournal.github.io/releases) برو و آخرین نسخه را دانلود کن.
2. فایل مناسب سیستم خودت را بردار:

| فایل | مناسب برای |
|---|---|
| `MT4 Journal-Setup-x64-<version>.exe` | ویندوز ۶۴ بیتی (پیشنهادی — اکثر سیستم‌ها) |
| `MT4 Journal-Setup-arm64-<version>.exe` | ویندوز روی دستگاه‌های ARM |
| `MT4 Journal-Setup-<version>.exe` | ترکیبی (هر دو معماری) |

3. نصاب را اجرا کن، پوشه نصب را انتخاب کن و تمام. هیچ پیش‌نیاز اضافه‌ای لازم نیست.

### 🚀 راه‌اندازی — اتصال خودکار به متاتریدر

بعد از نصب فقط **یک بار** این مراحل را انجام بده؛ از این به بعد همه‌چیز خودکار است:

1. برنامه را اجرا کن. در اولین اجرا مسیر فایل `terminal.exe` متاتریدرت را وارد کن (یا با دکمه Browse انتخابش کن).
2. روی **Auto-install EA in MetaTrader** بزن — برنامه خودش اکسپرت `Mt4JournalExporter` را داخل پوشه متاتریدر کپی و کامپایل می‌کند.
3. در متاتریدر، اکسپرت `Mt4JournalExporter` را از *Navigator → Expert Advisors* روی هر چارتی بینداز.
4. در تب *Account History* راست‌کلیک کن و **All History** را بزن تا کل تاریخچه هم وارد شود.
5. تمام! ✅ هر معامله‌ای که بسته شود، ظرف چند ثانیه به‌صورت خودکار در ژورنال ثبت می‌شود.

**چطور کار می‌کند؟** اکسپرت هر معامله بسته‌شده را در یک فایل CSV داخل پوشه متاتریدر می‌نویسد و برنامه هر چند ثانیه آن را می‌خواند و در دیتابیس محلی SQLite ذخیره می‌کند. اطلاعات تو (یادداشت‌ها، ریوارد، استراتژی، عکس‌ها) موقع سینک مجدد حفظ می‌شوند و هیچ داده‌ای هرگز جایی آپلود نمی‌شود.

#### روش جایگزین — بدون اکسپرت

اگر نمی‌خواهی از اکسپرت استفاده کنی: در متاتریدر روی *Account History* راست‌کلیک → **All History** → **Save as Report**، بعد در برنامه گزینه **Import HTML Report** را بزن.

#### اگر پوشه متاتریدر پیدا نشد

در تنظیمات برنامه مسیر پوشه‌ای که شامل `MQL4` است را دستی وارد کن — معمولاً:

```
%APPDATA%\MetaQuotes\Terminal\<TERMINAL_HASH>
```

### 🛠 استفاده روزمره

- **هیچ کاری لازم نیست** — معاملات خودشان ثبت می‌شوند.
- روی هر معامله کلیک کن تا **یادداشت** بنویسی (دلیل ورود، اشتباهات، درس‌ها)، **ریوارد** بدهی و **اسکرین‌شات چارت** اضافه کنی.
- **استراتژی‌هایت را تعریف کن** و به هر معامله اختصاص بده؛ جدول و آمار بر اساس استراتژی فیلتر می‌شوند.
- در صفحه **آمار**: سود خالص، نرخ برد، فاکتور سود، تقویم معاملاتی ماهانه و نمودارهای روزانه / ماهانه / نمادها / منحنی رشد را ببین.
- تاریخ‌ها با **تقویم شمسی** و ساعت ایران نمایش داده می‌شوند (حالت میلادی هم هست).
- از نوار ابزار بین **چند حساب** جابه‌جا شو و زبان برنامه (فارسی/انگلیسی) را عوض کن.

### 🔒 حریم خصوصی

دیتابیس و عکس‌ها فقط به‌صورت لوکال کنار برنامه ذخیره می‌شوند. برنامه نیازی به اینترنت ندارد و هیچ داده‌ای به هیچ سروری ارسال نمی‌شود.

---

## 📄 License

MIT © [mtjournal](https://github.com/mtjournal)
