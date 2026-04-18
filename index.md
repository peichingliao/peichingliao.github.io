---
# FlySP privacy policy (bilingual zh-TW / en).
# Publish to your GitHub Pages repo as `index.md`.
layout: default
title: FlySP Privacy Policy
---

# FlySP — 隱私權政策 / Privacy Policy

**生效日 / Effective Date:** 2026-04-18
**最後更新 / Last Updated:** 2026-04-18

---

## 繁體中文版

### 1. 前言

FlySP（以下簡稱「本應用程式」）是一款提供 GPS 位置模擬功能的行動應用程式，套件名稱為 `com.pcliao.flysp`。本政策說明我們如何收集、使用、儲存與保護您的個人資料。

使用本應用程式即表示您同意本隱私權政策之內容。

### 2. 我們收集的資訊

#### 2.1 位置資訊
- **何時收集**：僅當您主動點擊「我的位置」按鈕時
- **目的**：將地圖中心移至您的實際位置，方便您選定目的地
- **儲存**：不上傳、不記錄，僅於當下查詢 GPS 並顯示於本機介面

#### 2.2 最愛位置（本機儲存）
- **內容**：您自行新增或匯入的位置座標、備註、國家、時區
- **儲存位置**：僅儲存於您裝置的本機儲存空間（`SharedPreferences`），未加密
- **用途**：顯示於您的「最愛」清單

#### 2.3 搜尋歷史（本機儲存）
- **內容**：您在應用內搜尋的文字關鍵字（最多 10 筆）
- **儲存位置**：僅儲存於本機 `SharedPreferences`
- **用途**：提供搜尋建議

#### 2.4 購買資訊
- **內容**：透過 Google Play 完成的「移除廣告」一次性購買之 `purchaseToken`
- **儲存位置**：透過 `flutter_secure_storage` 儲存於 Android Keystore（加密）
- **用途**：於您每次啟動 app 時向 Google Play 驗證您的購買狀態

#### 2.5 廣告識別碼（AAID）
- **由誰收集**：Google AdMob（第三方）
- **用途**：提供個人化廣告；您可於 Android 系統設定中重設或關閉
- **我們的立場**：我們**不直接收集**此識別碼，亦不會對其進行任何分析

### 3. 第三方服務

| 服務 | 用途 | 隱私權政策連結 |
|------|------|----------------|
| Google Mobile Ads (AdMob) | 顯示廣告；識別已付費移除廣告用戶 | https://policies.google.com/privacy |
| Google Play Billing | 處理「移除廣告」一次性購買 | https://policies.google.com/privacy |
| OpenStreetMap (Nominatim) | 位置搜尋 | https://wiki.openstreetmap.org/wiki/Privacy_Policy |
| OSRM | 路徑規劃 | https://project-osrm.org |
| OpenStreetMap Tiles | 地圖圖磚 | https://operations.osmfoundation.org/policies/tiles |

### 4. 我們「不」做的事

- ❌ 我們**不會**上傳您的位置到任何伺服器
- ❌ 我們**不會**將您的最愛或搜尋歷史分享給任何第三方
- ❌ 我們**不會**對您進行跨 App 追蹤
- ❌ 我們**沒有**任何後端伺服器收集您的個人資料
- ❌ 我們**不會**販售您的任何資訊

### 5. 資料儲存位置與安全

- **本機儲存**：最愛、搜尋歷史、app 偏好設定
- **加密儲存 (Android Keystore)**：付費狀態、Google Play 購買 Token
- **離開裝置的資料**：僅限第三方服務查詢時所需的最小資料（例如搜尋關鍵字傳給 OpenStreetMap）

解除安裝本應用程式將刪除所有本機儲存的資料。

### 6. 兒童隱私（COPPA）

本應用程式**不針對未滿 13 歲之兒童**設計，我們**不會**刻意收集 13 歲以下兒童的個人資料。若您認為孩童未經同意在本 App 中提供了資訊，請透過下方聯絡方式告知我們刪除。

### 7. 歐盟使用者（GDPR）與加州使用者（CCPA）

若您位於歐盟、英國或加利福尼亞州，您享有以下權利：
- 請求存取我們持有的您的個人資料
- 請求修正或刪除您的資料
- 反對或限制處理
- 資料可攜權（取得您資料的副本）

由於本 App **不在伺服器儲存個人資料**，所有資料都在您的裝置本機；您可透過以下方式自行行使權利：
- 於 app 內刪除個別最愛、清除搜尋歷史
- 於系統設定中清除 app 資料
- 解除安裝 app

### 8. 所需權限說明

| Android 權限 | 用途 |
|-------------|------|
| `ACCESS_FINE_LOCATION` / `ACCESS_COARSE_LOCATION` | 取得您的實際位置（僅於您點擊「我的位置」時）|
| `ACCESS_MOCK_LOCATION` | 讓系統將本 App 列入「選取模擬位置應用程式」選單，需您於開發者選項中主動授權 |
| `INTERNET` / `ACCESS_NETWORK_STATE` | 地圖圖磚、搜尋、路徑規劃、廣告 |
| `FOREGROUND_SERVICE` / `FOREGROUND_SERVICE_SPECIAL_USE` | 維持位置模擬在背景持續執行 |
| `WAKE_LOCK` | 避免裝置休眠中止位置模擬 |
| `POST_NOTIFICATIONS` | 顯示背景服務通知與長時間模擬提醒 |
| `BILLING` | 處理「移除廣告」購買 |
| `AD_ID` | 由 AdMob SDK 使用（可於系統設定關閉）|

### 9. 政策變更

我們可能不時更新本政策。重大變更時，將於本網頁更新「最後更新」日期並於應用程式內通知您。

### 10. 聯絡方式

如有任何關於本政策的問題，請透過以下方式聯絡：

**Email**: `sylvia.pc.liao@gmail.com`

---

## English Version

### 1. Introduction

FlySP ("the App", package `com.pcliao.flysp`) is a mobile application that provides GPS location simulation. This policy explains how we collect, use, store, and protect your personal information.

By using the App, you agree to this Privacy Policy.

### 2. Information We Collect

#### 2.1 Location Information
- **When**: Only when you explicitly tap the "My Location" button
- **Purpose**: To center the map on your actual position so you can pick destinations
- **Storage**: Not uploaded. GPS is queried on-demand and displayed locally only.

#### 2.2 Favorite Locations (local only)
- **Contents**: Coordinates, notes, country, and timezone you add or import
- **Where stored**: Your device's local `SharedPreferences` only (unencrypted)
- **Purpose**: Display your "Favorites" list

#### 2.3 Search History (local only)
- **Contents**: Your search keywords (up to 10 entries)
- **Where stored**: Device-local `SharedPreferences`
- **Purpose**: Provide search suggestions

#### 2.4 Purchase Information
- **Contents**: `purchaseToken` for the one-time "Remove Ads" purchase via Google Play
- **Where stored**: Android Keystore via `flutter_secure_storage` (encrypted)
- **Purpose**: Verify your purchase status with Google Play on each app launch

#### 2.5 Advertising ID (AAID)
- **Collected by**: Google AdMob (third-party)
- **Purpose**: Personalized ads; you can reset or opt out in Android system settings
- **Our stance**: We **do not directly collect** this identifier and perform no analytics on it.

### 3. Third-Party Services

| Service | Purpose | Privacy Policy |
|---------|---------|----------------|
| Google Mobile Ads (AdMob) | Show ads; honor ad-free purchase | https://policies.google.com/privacy |
| Google Play Billing | Process "Remove Ads" purchase | https://policies.google.com/privacy |
| OpenStreetMap Nominatim | Location search | https://wiki.openstreetmap.org/wiki/Privacy_Policy |
| OSRM | Route planning | https://project-osrm.org |
| OpenStreetMap Tiles | Map tiles | https://operations.osmfoundation.org/policies/tiles |

### 4. What We Do NOT Do

- ❌ We do **not** upload your location to any server
- ❌ We do **not** share your favorites or search history with any third party
- ❌ We do **not** track you across apps
- ❌ We have **no** backend server collecting your personal data
- ❌ We do **not** sell any of your information

### 5. Data Storage & Security

- **Local storage**: favorites, search history, app preferences
- **Encrypted storage (Android Keystore)**: purchase status and Google Play purchase token
- **Data leaving the device**: only the minimum required to query third-party services (e.g. search keywords sent to OpenStreetMap)

Uninstalling the App deletes all locally-stored data.

### 6. Children's Privacy (COPPA)

The App is **not directed to children under 13**. We do not knowingly collect personal information from children under 13. If you believe a child has provided information in the App without consent, please contact us to remove it.

### 7. EU Users (GDPR) and California Users (CCPA)

If you reside in the EU, UK, or California, you have the right to:
- Request access to the personal data we hold about you
- Request correction or deletion
- Object to or restrict processing
- Data portability (obtain a copy of your data)

Since the App **does not store personal data on any server**, all data lives on your device. You can exercise these rights yourself by:
- Deleting individual favorites / clearing search history in-app
- Clearing app data in system settings
- Uninstalling the App

### 8. Permissions Explained

| Android Permission | Purpose |
|-------------------|---------|
| `ACCESS_FINE_LOCATION` / `ACCESS_COARSE_LOCATION` | Read your actual GPS (only when you tap "My Location") |
| `ACCESS_MOCK_LOCATION` | Let Android list this app in Developer Options → "Select mock location app"; still requires your explicit opt-in |
| `INTERNET` / `ACCESS_NETWORK_STATE` | Map tiles, search, routing, ads |
| `FOREGROUND_SERVICE` / `FOREGROUND_SERVICE_SPECIAL_USE` | Keep location simulation running in background |
| `WAKE_LOCK` | Prevent device sleep from interrupting simulation |
| `POST_NOTIFICATIONS` | Show the background service notification and long-simulation reminders |
| `BILLING` | Handle "Remove Ads" in-app purchase |
| `AD_ID` | Used by the AdMob SDK (opt-out available in system settings) |

### 9. Changes to This Policy

We may update this policy from time to time. Material changes will be reflected in the "Last Updated" date above and announced in-app where appropriate.

### 10. Contact

For any questions about this policy, contact us at:

**Email**: `sylvia.pc.liao@gmail.com`

---

<sub>© 2026 FlySP. All trademarks belong to their respective owners.</sub>
