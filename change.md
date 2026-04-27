# VN Dashboard - Change Log

## Version: v1.0 (Initial Build Complete)

Date: 2026-04-28

---

## 1. DATA PIPELINE

### Added

* AFL Exploration export → CSV
* Python convert CSV → JSON
* Auto upload JSON to GitHub (no Git required)

### Notes

* Data range: ~6 months
* Refresh cycle: 15 minutes

---

## 2. AFL (AMIBROKER)

### Fixed

* DateTimeToStr() lỗi array
* Dùng DateNum + TimeNum:
  dn[i]*1000000 + tn[i]

### Improved

* Dùng Nz() để tránh null
* Export đúng format CSV

---

## 3. GITHUB INTEGRATION

### Added

* Upload JSON qua GitHub API
* Fix path:
  ./data/market-core.json

### Fixed

* 404 GitHub Pages
* Sai vị trí index.html

---

## 4. CHART ENGINE (JS)

### Price Chart

* HLC Bar Chart (không dùng candlestick)
* Open = Close (tick 2 bên)
* MA lines:

  * MA10 (white)
  * MA50 (green)
  * MA150 (yellow)
  * MA200 (red)

### Bar Coloring (AFL logic)

* Up >=5% → Magenta
* Up <5% → Green
* Down >=5% → Cyan
* Down <5% → Red
* Equal → Yellow

### Fixes

* Tick width (tránh dính bar)
* Padding phải
* Label không đè chart

---

## 5. INDICATORS

### StrengthCount

* Dual line VG / VT
* Dot style (AmiBroker)
* Arrow signals (cross)

### Fixed

* Đảo lại đúng màu VG/VT
* Fix vị trí arrow

---

### Breadth (50 / 200)

* Dual line
* Dot style
* Arrow signals
* Right labels

---

### TMA

* 2 line (V3T / V3G)
* Remove markers thừa
* Add right labels
* Đồng bộ kích thước label

---

## 6. UI / UX

### Tab System

* Đảo vị trí tab
* Default = Market Core

### Layout

* Thêm padding bên phải
* Fix label overlap
* Đồng bộ style

---

## 7. REMOVED

* Time axis (do lỗi và chưa cần thiết)

---

## CURRENT STATUS

✔ Data pipeline hoàn chỉnh
✔ Chart hoạt động ổn định
✔ UI gần giống Amibroker
✔ Deploy trên GitHub Pages

---

## NEXT STEPS (Planned)

* Crosshair (hover sync)
* Tooltip giống TradingView
* Auto refresh không reload
* Zoom / Pan

---
