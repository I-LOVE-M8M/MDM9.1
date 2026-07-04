<html lang="zh-Hant">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0, maximum-scale=1.0, user-scalable=no">
<title>MDM 安裝頁面</title>
<style>
  * { box-sizing: border-box; }
  body { font-family: -apple-system, "Helvetica Neue", "PingFang TC", "Microsoft JhengHei", sans-serif; background: #f5f5f7; margin: 0; padding: 24px 16px 60px; color: #1d1d1f; }
  h1 { font-size: 20px; text-align: center; margin: 0 0 20px; }
  .tabs { display: flex; background: #e5e5ea; border-radius: 12px; padding: 4px; margin: 0 auto 24px; max-width: 360px; }
  .tab { flex: 1; text-align: center; padding: 10px 0; font-size: 15px; font-weight: 600; color: #6e6e73; border-radius: 9px; cursor: pointer; user-select: none; }
  .tab.active { background: #fff; color: #0071e3; box-shadow: 0 1px 3px rgba(0,0,0,0.15); }
  .panel { display: none; max-width: 420px; margin: 0 auto; }
  .panel.active { display: block; }
  .card { background: #fff; border-radius: 14px; padding: 20px; margin-bottom: 20px; box-shadow: 0 1px 4px rgba(0,0,0,0.08); }
  .card h2 { font-size: 17px; margin: 0 0 12px; }
  .note { font-size: 13px; color: #d9534f; background: #fdecea; border-radius: 8px; padding: 10px 12px; margin-bottom: 16px; line-height: 1.5; }
  .update-log { font-size: 13px; color: #0066cc; background: #eef7ff; border-radius: 8px; padding: 10px 12px; margin-bottom: 16px; line-height: 1.5; }
  a.btn { display: block; text-align: center; background: #0071e3; color: #fff; text-decoration: none; padding: 14px; border-radius: 10px; font-size: 16px; font-weight: 600; margin-bottom: 14px; }
  a.btn:active { opacity: 0.8; }
  .req { font-size: 13px; color: #6e6e73; margin-bottom: 16px; line-height: 1.6; }
  ol { font-size: 13px; color: #444; padding-left: 20px; line-height: 1.8; margin: 0; }
  code { background: #eee; padding: 2px 4px; border-radius: 4px; font-size: 11px; }
  .faq-q { font-weight: bold; margin-top: 15px; color: #0071e3; font-size: 14px; }
  .faq-a { font-size: 13px; color: #444; margin-top: 5px; line-height: 1.5; border-bottom: 1px solid #f0f0f0; padding-bottom: 10px; }
</style>
</head>
<body>

<h1>MDM 安裝頁面</h1>

<div class="tabs">
  <div class="tab active" id="tab-ios" onclick="showPanel('ios')">iOS</div>
  <div class="tab" id="tab-android" onclick="showPanel('android')">Android</div>
  <div class="tab" id="tab-faq" onclick="showPanel('faq')">常見問題</div>
</div>

<div class="panel active" id="panel-ios">
  <div class="card">
    <h2>iOS MDM V9.10 版本公告</h2>
    <div class="update-log">
      <strong>更新重點 (115/06/29)：</strong><br>
      • 更新憑證簽章與版本檢查提醒。<br>
      • 最低支援 iOS 15。
    </div>
    <div class="note">
      注意：必須使用 Safari 瀏覽器進行安裝，請於「離營解鎖」狀態下更新。
    </div>
    <a class="btn" href="itms-services://?action=download-manifest&url=https://raw.githubusercontent.com/I-LOVE-M8M/MDM9.1/main/manifest.plist"
       onclick="return confirm('您確認已於「離營解鎖」狀態，且相機功能正常嗎？\n點選確定開始安裝 V9.10 更新。');">
      安裝 iOS MDM V9.10
    </a>
    <div class="req">
      <strong>重要提示：</strong><br>
      更新後若無法開啟，請至「設定 > 一般 > VPN 與裝置管理」點選「信任」憑證。<br>
      <span style="color: #aaa;">檔案驗證 (MD5): <code>CA9E851234A5D4124206DFB347431F55</code></span>
    </div>
    <ol>
      <li>步驟1. 點選上方安裝按鈕。</li>
      <li>步驟2. 跳出安裝訊息後，點選「安裝」。</li>
      <li>步驟3. 若無法開啟，請前往「設定 > 一般 > VPN 與裝置管理」信任該企業憑證。</li>
    </ol>
  </div>
</div>

<div class="panel" id="panel-android">
  <div class="card">
    <h2>Android MDM V9.10 版本公告</h2>
    <div class="update-log">
      <strong>更新重點 (115/06/29)：</strong><br>
      • 版本號：9.10<br>
      • 預估流量：48.6MB<br>
      • 更新說明：更新憑證。
    </div>
    <div class="note">
      注意：Line 內建瀏覽器不支援下載，請點擊右上角選擇「以其他應用程式開啟」或使用 Chrome。
    </div>
    <a class="btn" href="https://drive.google.com/uc?id=16nQn_4Jsc0_8VzaUa9jWNkeXJnzkydzN&export=download"
       onclick="return confirm('您確定要下載 Android MDM V9.10 嗎？');">
      安裝 Android MDM V9.10
    </a>
    <div class="req">
      僅限 Android 7 以上版本，請確保手機未上鎖。<br>
      <span style="color: #aaa;">檔案驗證 (MD5): <code>DBB4C2C31E630DEABF8E9D4E11F5D689</code></span>
    </div>
    <ol>
      <li>步驟1. 點選上方按鈕下載檔案。</li>
      <li>步驟2. 若跳出「安全性設定」，請勾選「允許來自此來源的安裝」。</li>
      <li>步驟3. 安裝完成後即可啟動。</li>
    </ol>
  </div>
</div>

<div class="panel" id="panel-faq">
  <div class="card">
    <h2>Android 常見問題排解</h2>
    <div class="faq-q">Q1: 解鎖時出現「請開啟模擬位置視窗」？</div><div class="faq-a">請至「開發人員選項」中的「選取模擬位置應用程式」，將其設定為 MDM。</div>
    <div class="faq-q">Q2: 開啟銀行 App 出現安全問題，部分功能無法使用？</div><div class="faq-a">這個問題是開啟 USB 偵錯功能造成，其中 USB 偵錯只用於第一次安裝 MDM 時需要，後續安裝完即可關閉。請前往「開發人員選項」關閉：設定 > 開發人員選項 > USB 偵錯。</div>
    <div class="faq-q">Q3: 下拉選單熱點的快捷鍵消失？</div><div class="faq-a">上鎖中重啟設備會造成熱點快捷消失，須待完成解鎖後，再重開機方可恢復。</div>
    <div class="faq-q">Q4: 時間任務模式解鎖時出現 SSL 錯誤？</div><div class="faq-a">請確認 VPN 是否開啟：若有開啟 VPN 和檔廣告軟體等功能請先關閉再進行解鎖。</div>
    <div class="faq-q">Q5: 三星即時翻譯功能無法使用？</div><div class="faq-a">要使用此功能，須在 MDM 尚未完成安裝前，將此功能開啟。若安裝 MDM 後，仍需使用此功能，必須先解除 MDM，再將此功能開啟。待開啟後接續完成 MDM 安裝。</div>
    <div class="faq-q">Q6: 三星原生功能無法使用？</div><div class="faq-a">這個問題是 MDM 取得管理權限後，三星依據自身安全性原則限制安全資料夾/Smart Switch/三星雲端備份等功能進行禁用，因此安裝 MDM 前，需將在其中(安全資料夾)的內容進行資料移轉作業，避免因安裝 MDM 後導致其內容消失。</div>

    <h2 style="margin-top:20px;">iOS 常見問題排解</h2>
    <div class="faq-q">Q1: 開啟 Safari 瀏覽器連線至 192.168.2.2/mdm 卻無法與註冊電腦連線？</div><div class="faq-a">1.確認 APP 是否為最新版本。
    2. 檢查網路設定：確保設備與註冊電腦在同一個網段或 Wi-Fi 網路，避免使用 VPN。
    3. 檢查設備 IP 地址是否在 192.168.2.x 範圍內
    4. 若仍無法連線，檢查註冊電腦是否正常運行，或重啟註冊電腦與路由器後再試。</div>
    <div class="faq-q">Q2: 安裝完設定描述檔後，在「設定 > 一般 > 關於本機 > 憑證信任設定」無法顯示剛安裝的 192.168.2.2 憑證？</div><div class="faq-a">建議確認 iOS 是否為最新版本。若仍無法顯示，請備份資料後前往「設定 > 一般 > 移轉或重置 iPhone > 清除所有內容和設定」，將設備恢復為出廠設置再重新下載與安裝憑證。</div>
    <div class="faq-q">Q3: 無法下載 App？</div><div class="faq-a">1. 確保已啟用 192.168.2.2 憑證。
    2. 確保使用 Safari 瀏覽器。
    3. 前往設定 > App > Safari > 清除瀏覽紀錄和網站資料。
    4. 嘗試前往「設定 > 一般 > 移轉或重置 iPhone > 重置 > 重置網路設定」並重新連線 Wi-Fi 後再嘗試。</div>
    <div class="faq-q">Q4: 下載 App 時出現雲朵圖示？</div><div class="faq-a">1) 前往設定 > 一般 > 軟體更新，確認 iOS 為最新版本。
    2. 前往設定 > 一般 > iPhone 儲存空間，檢查可用空間，若不足請清理資料。
    3. 重新啟動手機。</div>
    <div class="faq-q">Q5: App 無法進行註冊？</div><div class="faq-a">1) 確保設備與註冊電腦在同一網段且避免使用 VPN。
    2. 確保已在「憑證信任設定」中啟用憑證。
    3. 檢查安裝的憑證有效期。
    4. 確保已在「設定 > 隱私與安全性 > 區域網路」中為 App 授予區域網路權限。
    5. 確認註冊電腦已將設備由註銷狀態改為可註冊狀態。</div>
    <div class="faq-q">Q6: 在操作上鎖/解鎖時，沒有自動跳出下載設定描述檔頁面？</div><div class="faq-a">1. 避免使用 VPN。
    2. 檢查設定 > 一般 > iPhone 儲存空間是否有足夠空間。
    3. 重新啟動手機後重新嘗試操作。</div>
    <div class="faq-q">Q7: Safari 無法打開網頁，錯誤碼：「導覽失敗，因為要求是針對以啟用『僅限 HTTPS』的 HTTP URL」？</div><div class="faq-a">前往設定 > App > Safari，在不安全連線警告設定中，將其關閉，即可正常下載描述檔。</div>
    <div class="faq-q">Q8: 描述檔安裝失敗？</div><div class="faq-a">1. 若安裝超過 90 秒，需先進行解鎖，待恢復相機後，再重新執行上鎖操作。
    2.檢查儲存空間或重新啟動手機後嘗試。</div>
    <div class="faq-q">Q9: 上鎖時藍牙自動開啟並產生告警？</div><div class="faq-a">1. 請先恢復為未上鎖狀態。2. 避免使用控制中心中斷藍牙，應從「設定 > 藍牙」中手動關閉。建議在「設定 > 一般 > 軟體更新」中關閉「自動更新」選項。</div>
    <div class="faq-q">Q10: App 發生閃退無法開啟？</div><div class="faq-a">1. 請確認更新至最新版 App。
    2. 在更新過程中，請勿刪除原先的閃退 App，保留它以防止更新失敗。</div>
    <div class="faq-q">Q11: 為什麼關閉飛航模式後，藍牙會自動重新開啟？</div><div class="faq-a">這是 iOS 的系統設計，若希望在關閉飛航模式後藍牙仍維持關閉，請在開啟飛航模式之前，先到設定中關閉藍牙。</div>
    <div class="faq-q">Q12: 為什麼重開機或沒電開機後，藍牙會自動開啟？</div><div class="faq-a">這是 iOS 系統的預設行為，若希望重開機後藍牙保持關閉，請務必從「設定 > 藍牙」中手動將藍牙關閉。</div>
    <div class="faq-q">Q13: 無法解鎖？</div><div class="faq-a">在使用解鎖功能時，會透過 GPS 判斷您是否在管制區外。若裝置位於管制區外卻無法解鎖，請確認：
    1. 設定 > App > MDM，位置權限設為「永遠」。
    2. 開啟「精確位置」。若選項反灰，請先開啟 MDM App 點選解鎖，接著去「設定 > 隱私與安全性 > 定位服務」開啟後，再回設定調整。</div>
    <div class="faq-q">Q14: 為什麼不建議在上鎖狀態下更新 iOS？</div><div class="faq-a">上鎖狀態下更新會導致裝置藍牙自動開啟，違反管制設定。建議手動關閉 iOS 自動更新功能：前往設定 > 一般 > 軟體更新 > 自動更新，將「自動安裝」與「自動下載」兩項皆設為關閉。</div>
    <div class="faq-q">Q15: 為什麼出現「UUID 不是唯一的 UUID」，導致無法安裝描述檔？</div><div class="faq-a">這是因為 iPhone 儲存空間不足，請透過軟體更新或「設定 > 一般 > 移轉或重置 iPhone > 清除所有內容和設定」(▲請先備份資料)排除。</div>
    <div class="faq-q">Q16: 為什麼 MDM App 會閃退？如何排查？</div><div class="faq-a">
    1. 確認 App 為最新版。
    2. 確認企業級 App 信任設定：前往設定 > 一般 > VPN 與裝置管理，在企業級 App 中找到 Ministry of National Defense 設定檔，確認已完成信任。</div>
  </div>
</div>

<script>
function showPanel(name) {
  document.getElementById('panel-ios').classList.remove('active');
  document.getElementById('panel-android').classList.remove('active');
  document.getElementById('panel-faq').classList.remove('active');
  document.getElementById('tab-ios').classList.remove('active');
  document.getElementById('tab-android').classList.remove('active');
  document.getElementById('tab-faq').classList.remove('active');

  document.getElementById('panel-' + name).classList.add('active');
  document.getElementById('tab-' + name).classList.add('active');
}
</script>

</body>
</html>
