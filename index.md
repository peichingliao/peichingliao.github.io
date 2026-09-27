---
# FlySP privacy policy (bilingual zh-TW / en).
# Publish to your GitHub Pages repo as `index.md`.
layout: default
title: FlySP Privacy Policy
---

# FlySP — 隱私權政策 / Privacy Policy

**生效日 / Effective Date:** 2026-04-18
**最後更新 / Last Updated:** 2026-09-18

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
- **儲存位置**：您裝置的本機儲存空間（`SharedPreferences`），未加密；並會納入 Android Auto Backup 備份到您自己的 Google 帳號（見第 5 節）
- **用途**：顯示於您的「最愛」清單

#### 2.3 搜尋歷史（本機儲存）
- **內容**：您在應用內搜尋的文字關鍵字（最多 10 筆）
- **儲存位置**：本機 `SharedPreferences`；同樣會納入 Android Auto Backup（見第 5 節）
- **用途**：提供搜尋建議

#### 2.4 購買資訊
- **內容**：透過 Google Play 完成的「移除廣告」一次性購買之 `purchaseToken`
- **儲存位置**：透過 `flutter_secure_storage` 儲存於 Android Keystore（加密）
- **用途**：於您每次啟動 app 時向 Google Play 驗證您的購買狀態

#### 2.5 廣告識別碼（AAID）
- **由誰收集**：Google AdMob（第三方）
- **用途**：提供個人化廣告；您可於 Android 系統設定中重設或關閉
- **我們的立場**：我們**不直接收集**此識別碼，亦不會對其進行任何分析

#### 2.6 健康資料（步數）
- **內容**：模擬移動過程所產生的步數
- **方向**：**只寫入、不讀取**。本 App 僅宣告 `android.permission.health.WRITE_STEPS`，並未取得任何讀取健康資料的權限，無法看到您既有的健康紀錄
- **儲存位置**：您裝置上的 Health Connect（由 Google 提供，不由本 App 持有）
- **何時發生**：僅在您於 App 內主動開啟「步數同步」並授權時
- **刪除方式**：於 Health Connect App 內刪除該筆資料，或撤銷本 App 的授權

### 3. 第三方服務

| 服務 | 用途 | 隱私權政策連結 |
|------|------|----------------|
| Google Mobile Ads (AdMob) | 顯示廣告；識別已付費移除廣告用戶 | https://policies.google.com/privacy |
| Google Play Billing | 處理「移除廣告」一次性購買 | https://policies.google.com/privacy |
| OpenStreetMap (Nominatim) | 位置搜尋 | https://wiki.openstreetmap.org/wiki/Privacy_Policy |
| OSRM | 路徑規劃 | https://project-osrm.org |
| OpenStreetMap Tiles | 地圖圖磚 | https://operations.osmfoundation.org/policies/tiles |
| Photon (komoot) | 位置搜尋與地名反查 | https://photon.komoot.io |
| Health Connect (Google) | 寫入模擬產生的步數（僅在您開啟步數同步時） | https://policies.google.com/privacy |

### 4. 我們「不」做的事

- ❌ 我們**不會**上傳您的位置到任何伺服器
- ❌ 我們**不會**將您的最愛或搜尋歷史分享給任何第三方
- ❌ 我們**不會**對您進行跨 App 追蹤
- ❌ 我們**沒有**任何後端伺服器收集您的個人資料
- ❌ 我們**不會**販售您的任何資訊

### 5. 資料儲存位置與安全

- **本機儲存**：最愛位置、搜尋歷史、模擬紀錄、app 偏好設定（存於 `SharedPreferences`）；最愛路徑存於本機資料庫 `flysp.db`
- **加密儲存 (Android Keystore)**：付費狀態、Google Play 購買 Token
- **離開裝置的資料**：
  - 第三方服務查詢時所需的最小資料（例如搜尋關鍵字傳給 OpenStreetMap）
  - **Android Auto Backup（自 1.11.0 起）**：您的最愛位置、最愛路徑、分類與 app 偏好設定會由 Android 系統備份到**您自己的 Google 帳號**。備份的範圍僅限上述兩個檔案（`FlutterSharedPreferences.xml` 與 `flysp.db`）。備份由 Android 系統執行與保管，本應用程式**無法讀取**該備份的內容，我們也從未持有它。
  - **刻意排除、不會被備份**的資料：以 Android Keystore 加密的付費狀態與購買 Token（`flutter_secure_storage`；金鑰綁定裝置，還原到新機也解不開），以及懸浮視窗採集 pin 的暫存佇列（`pin_queue.json`；中繼狀態，還原後沒有意義）。
  - **如何關閉**：系統設定 → Google → 備份（部分機型為 設定 → 系統 → 備份），可關閉整台裝置的備份，或僅關閉本應用程式的備份。關閉後新的資料不再上傳，但既有的備份需另外刪除（見第 6 節）。

解除安裝本應用程式將刪除所有本機儲存的資料；但**已上傳到您 Google 帳號的備份不會隨之刪除**，它會一直保留到您自行刪除為止（刪除方式見第 6 節）。

### 6. 資料保留與刪除

**我們不保留您的任何個人資料。** 本應用程式沒有後端伺服器，不需要註冊帳號，也不會將您的最愛位置、搜尋歷史、模擬紀錄或任何裝置識別碼傳送到我們持有或控制的系統。我們沒有可以保留這些資料的地方。

下列資料儲存在**您的裝置上**，保留期間完全由您決定，直到您自行刪除為止（其中多數另有一份 Android Auto Backup 備份在您自己的 Google 帳號，說明見本節後段與第 5 節）：

| 資料類別 | 保留位置 | 保留期間 | 刪除方式 |
|---------|---------|---------|---------|
| 最愛位置 | 本機 `SharedPreferences` | 直到您刪除 | App 內逐筆刪除，或解除安裝 |
| 收藏路徑 | 本機資料庫 `flysp.db` | 直到您刪除 | App 內逐筆刪除，或解除安裝 |
| 搜尋歷史（最多 10 筆） | 本機 `SharedPreferences` | 直到您清除 | App 內清除搜尋歷史，或解除安裝 |
| 模擬紀錄 | 本機 `SharedPreferences` | 直到您刪除 | App 內於模擬歷史清單刪除，或解除安裝 |
| App 偏好設定（語言、功能開關） | 本機 `SharedPreferences` | 直到您重設 | 系統設定 → 應用程式 → FlySP → 清除資料，或解除安裝 |
| 購買狀態與 `purchaseToken` | Android Keystore（加密） | 直到您解除安裝 | 解除安裝 |

**解除安裝本應用程式會一併刪除上述全部儲存在裝置上的資料。** 由於我們從未持有這些資料，刪除後我們無從復原，您也不需要向我們提出刪除請求。

**但 Google 帳號中的備份是例外。** 上表中儲存於 `SharedPreferences` 與 `flysp.db` 的項目（最愛位置、收藏路徑、分類、搜尋歷史、模擬紀錄、app 偏好設定）同時會被 Android Auto Backup 複製到您自己的 Google 帳號（見第 5 節）。這份備份**不會因為您解除安裝本應用程式而消失**——那正是它的用途：讓您換機或重裝時資料回得來。它保留在您的 Google 帳號中，直到您自行刪除；我們無法讀取，也無法代為刪除。

刪除該備份的方式（皆在本應用程式之外，由您直接操作 Google）：

| 目的 | 操作路徑 |
|------|---------|
| 刪除已存在的備份 | Google One App → 儲存空間 → 裝置備份 → 選擇該裝置 →（選擇本應用程式的資料或整份備份）→ 刪除 |
| 停止之後再上傳 | 系統設定 → Google → 備份 → 關閉「App 資料備份」或整個備份功能 |

若您希望裝置上與備份中都不留下任何資料：先於系統設定關閉備份並刪除既有備份，再解除安裝本應用程式。

位置資訊（見 2.1）**不會被保留**：僅在您點擊「我的位置」時查詢一次並顯示於畫面，不寫入任何儲存空間。

第三方服務（見第 3 節）依其各自的隱私權政策保留資料，不在我們的控制範圍內；其保留做法請參閱該節所列的政策連結。

### 7. 兒童隱私（COPPA）

本應用程式**不針對未滿 13 歲之兒童**設計，我們**不會**刻意收集 13 歲以下兒童的個人資料。若您認為孩童未經同意在本 App 中提供了資訊，請透過下方聯絡方式告知我們刪除。

### 8. 歐盟使用者（GDPR）與加州使用者（CCPA）

若您位於歐盟、英國或加利福尼亞州，您享有以下權利：
- 請求存取我們持有的您的個人資料
- 請求修正或刪除您的資料
- 反對或限制處理
- 資料可攜權（取得您資料的副本）

由於本 App **不在伺服器儲存個人資料**，所有資料都在您的裝置本機；您可透過以下方式自行行使權利：
- 於 app 內刪除個別最愛、清除搜尋歷史
- 於系統設定中清除 app 資料
- 解除安裝 app
- 刪除您 Google 帳號中的 Android Auto Backup 備份（步驟見第 6 節）

### 9. 所需權限說明

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
| `health.WRITE_STEPS` | 將模擬產生的步數寫入 Health Connect（僅在您開啟步數同步時）|
| `SYSTEM_ALERT_WINDOW` | 顯示懸浮控制視窗（懸浮模式）|
| `VIBRATE` | 操作回饋震動 |

### 10. 政策變更

我們可能不時更新本政策。重大變更時，將於本網頁更新「最後更新」日期並於應用程式內通知您。

### 11. 聯絡方式

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

#### 2.2 Favorite Locations (on your device)
- **Contents**: Coordinates, notes, country, and timezone you add or import
- **Where stored**: Your device's local `SharedPreferences` (unencrypted); also included in Android Auto Backup to your own Google account (see Section 5)
- **Purpose**: Display your "Favorites" list

#### 2.3 Search History (on your device)
- **Contents**: Your search keywords (up to 10 entries)
- **Where stored**: Device-local `SharedPreferences`; also included in Android Auto Backup (see Section 5)
- **Purpose**: Provide search suggestions

#### 2.4 Purchase Information
- **Contents**: `purchaseToken` for the one-time "Remove Ads" purchase via Google Play
- **Where stored**: Android Keystore via `flutter_secure_storage` (encrypted)
- **Purpose**: Verify your purchase status with Google Play on each app launch

#### 2.5 Advertising ID (AAID)
- **Collected by**: Google AdMob (third-party)
- **Purpose**: Personalized ads; you can reset or opt out in Android system settings
- **Our stance**: We **do not directly collect** this identifier and perform no analytics on it.

#### 2.6 Health Data (Steps)
- **What**: step counts generated by simulated movement
- **Direction**: **write-only, never read.** The App declares only `android.permission.health.WRITE_STEPS` and holds no permission to read health data, so it cannot see your existing health records
- **Where stored**: Health Connect on your device (provided by Google, not held by us)
- **When**: only when you enable step sync in-app and grant permission
- **How to delete**: delete the entries in the Health Connect app, or revoke the App's permission

### 3. Third-Party Services

| Service | Purpose | Privacy Policy |
|---------|---------|----------------|
| Google Mobile Ads (AdMob) | Show ads; honor ad-free purchase | https://policies.google.com/privacy |
| Google Play Billing | Process "Remove Ads" purchase | https://policies.google.com/privacy |
| OpenStreetMap Nominatim | Location search | https://wiki.openstreetmap.org/wiki/Privacy_Policy |
| OSRM | Route planning | https://project-osrm.org |
| OpenStreetMap Tiles | Map tiles | https://operations.osmfoundation.org/policies/tiles |
| Photon (komoot) | Location search and reverse geocoding | https://photon.komoot.io |
| Health Connect (Google) | Writing simulated step counts (only when you enable step sync) | https://policies.google.com/privacy |

### 4. What We Do NOT Do

- ❌ We do **not** upload your location to any server
- ❌ We do **not** share your favorites or search history with any third party
- ❌ We do **not** track you across apps
- ❌ We have **no** backend server collecting your personal data
- ❌ We do **not** sell any of your information

### 5. Data Storage & Security

- **Local storage**: favorite locations, search history, simulation records and app preferences (in `SharedPreferences`); saved routes in a local database, `flysp.db`
- **Encrypted storage (Android Keystore)**: purchase status and Google Play purchase token
- **Data leaving the device**:
  - The minimum required to query third-party services (e.g. search keywords sent to OpenStreetMap)
  - **Android Auto Backup (since 1.11.0)**: your favorite locations, saved routes, categories and app preferences are backed up by the Android system to **your own Google account**. The backup covers only those two files (`FlutterSharedPreferences.xml` and `flysp.db`). The backup is performed and held by Android; the App **cannot read** its contents, and we never hold it.
  - **Deliberately excluded from the backup**: purchase status and purchase token held in Android Keystore (`flutter_secure_storage` — the key is device-bound and would not be decryptable after a restore), and the floating-window pin collection queue (`pin_queue.json` — transient state that means nothing once restored).
  - **How to turn it off**: system Settings → Google → Backup (on some devices, Settings → System → Backup). You can disable backup for the whole device or for this app only. Turning it off stops further uploads; an existing backup must be deleted separately (see Section 6).

Uninstalling the App deletes all locally-stored data; however, **a backup already uploaded to your Google account is not deleted with it**. It remains until you delete it yourself (see Section 6).

### 6. Data Retention and Deletion

**We do not retain any of your personal data.** The App has no backend server, requires no account, and does not transmit your favorites, search history, simulation records, or any device identifier to any system we own or control. There is nowhere for us to retain it.

The data below is stored **on your device**. You control how long it is kept; it remains until you delete it. (Most of it also has an Android Auto Backup copy in your own Google account — see the end of this section and Section 5.)

| Data | Where retained | Retention period | How to delete |
|------|---------------|------------------|---------------|
| Favorite locations | Local `SharedPreferences` | Until you delete them | Delete individually in-app, or uninstall |
| Saved routes | Local database `flysp.db` | Until you delete them | Delete individually in-app, or uninstall |
| Search history (max 10 entries) | Local `SharedPreferences` | Until you clear it | Clear search history in-app, or uninstall |
| Simulation records | Local `SharedPreferences` | Until you delete them | Delete from the simulation history list in-app, or uninstall |
| App preferences (language, toggles) | Local `SharedPreferences` | Until you reset them | System Settings → Apps → FlySP → Clear data, or uninstall |
| Purchase status and `purchaseToken` | Android Keystore (encrypted) | Until you uninstall | Uninstall |

**Uninstalling the App deletes all of the above from the device.** Because we never held this data, we cannot recover it after deletion, and you do not need to send us a deletion request.

**The backup in your Google account is the exception.** The items above that live in `SharedPreferences` and `flysp.db` (favorite locations, saved routes, categories, search history, simulation records, app preferences) are also copied to your own Google account by Android Auto Backup (see Section 5). That copy **does not disappear when you uninstall the App** — that is exactly its purpose: to bring your data back when you reinstall or switch devices. It stays in your Google account until you delete it; we can neither read it nor delete it for you.

How to delete that backup (all of this happens outside the App, directly with Google):

| Goal | Path |
|------|------|
| Delete an existing backup | Google One app → Storage → Device backups → pick the device → (pick this app's data, or the whole backup) → Delete |
| Stop future uploads | System Settings → Google → Backup → turn off "Backup by Google One" / app data backup |

If you want nothing left either on the device or in the backup: turn backup off and delete the existing backup in system settings first, then uninstall the App.

Location data (see 2.1) is **not retained**: it is queried once when you tap "My Location", shown on screen, and never written to storage.

Third-party services (see Section 3) retain data under their own privacy policies, outside our control; see the policy links in that section for their retention practices.

### 7. Children's Privacy (COPPA)

The App is **not directed to children under 13**. We do not knowingly collect personal information from children under 13. If you believe a child has provided information in the App without consent, please contact us to remove it.

### 8. EU Users (GDPR) and California Users (CCPA)

If you reside in the EU, UK, or California, you have the right to:
- Request access to the personal data we hold about you
- Request correction or deletion
- Object to or restrict processing
- Data portability (obtain a copy of your data)

Since the App **does not store personal data on any server**, all data lives on your device. You can exercise these rights yourself by:
- Deleting individual favorites / clearing search history in-app
- Clearing app data in system settings
- Uninstalling the App
- Deleting the Android Auto Backup copy in your Google account (steps in Section 6)

### 9. Permissions Explained

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
| `health.WRITE_STEPS` | Write simulated step counts to Health Connect (only when you enable step sync) |
| `SYSTEM_ALERT_WINDOW` | Show the floating control window (overlay mode) |
| `VIBRATE` | Haptic feedback |

### 10. Changes to This Policy

We may update this policy from time to time. Material changes will be reflected in the "Last Updated" date above and announced in-app where appropriate.

### 11. Contact

For any questions about this policy, contact us at:

**Email**: `sylvia.pc.liao@gmail.com`

---

<sub>© 2026 FlySP. All trademarks belong to their respective owners.</sub>
