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
  /* FAQ 專用樣式 */
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
    <h2>Android 常見問題</h2>
    <div class="faq-item"><div class="faq-q">Q1: 解鎖時出現「請開啟模擬位置視窗」？</div><div class="faq-a">請至「開發人員選項」將「選取模擬位置應用程式」設定為 MDM。</div></div>
    <div class="faq-item"><div class="faq-q">Q2: 開啟銀行 App 出現安全問題？</div><div class="faq-a">這是「USB 偵錯」造成，請至開發人員選項關閉該功能。</div></div>
    <div class="faq-item"><div class="faq-q">Q3: 下拉選單熱點快捷鍵消失？</div><div class="faq-a">此為上鎖狀態下對特定功能的限制。</div></div>
    <div class="faq-item"><div class="faq-q">Q4: 時間任務解鎖出現 SSL 錯誤？</div><div class="faq-a">檢查網路環境，關閉 VPN 或廣告攔截軟體。</div></div>
    <div class="faq-item"><div class="faq-q">Q5-Q6: 三星功能無法使用？</div><div class="faq-a">上鎖狀態限制部分三星原生功能與即時翻譯。</div></div>

    <h2 style="margin-top:20px;">iOS 常見問題</h2>
    <div class="faq-item"><div class="faq-q">Q1: 無法與註冊電腦連線？</div><div class="faq-a">確認設備與註冊電腦在同一 Wi-Fi 網段，且 IP 為 192.168.2.x。</div></div>
    <div class="faq-item"><div class="faq-q">Q2: 憑證無法信任或顯示？</div><div class="faq-a">確認 iOS 為最新版，或嘗試備份後清除內容與設定重新安裝。</div></div>
    <div class="faq-item"><div class="faq-q">Q3: 無法下載 App？</div><div class="faq-a">檢查 Safari 快取、儲存空間是否充足。</div></div>
    <div class="faq-item"><div class="faq-q">Q4: 下載 App 出現雲朵圖示？</div><div class="faq-a">代表 App 被卸載，請重新點擊安裝即可。</div></div>
    <div class="faq-item"><div class="faq-q">Q5: App 無法註冊？</div><div class="faq-a">確認已授予區域網路權限，且註冊電腦未將設備設為註銷。</div></div>
    <div class="faq-item"><div class="faq-q">Q6: 操作上鎖/解鎖無跳出視窗？</div><div class="faq-a">請恢復相機功能，並確認 Safari 正常運作。</div></div>
    <div class="faq-item"><div class="faq-q">Q7: Safari 顯示 HTTPS 錯誤？</div><div class="faq-a">請依照提示關閉 Safari「僅限 HTTPS」的安全性警告。</div></div>
    <div class="faq-item"><div class="faq-q">Q8: 描述檔安裝失敗？</div><div class="faq-a">安裝時效 90 秒，超時請重新執行。</div></div>
    <div class="faq-item"><div class="faq-q">Q9: 藍牙自動開啟告警？</div><div class="faq-a">MDM 上鎖機制會自動檢查藍牙狀態，請勿從控制中心中斷。</div></div>
    <div class="faq-item"><div class="faq-q">Q10: App 發生閃退？</div><div class="faq-a">請直接覆蓋安裝新版，勿刪除舊版。</div></div>
    <div class="faq-item"><div class="faq-q">Q11: 飛航模式後藍牙開啟？</div><div class="faq-a">請在開啟飛航前先從「設定」內關閉藍牙。</div></div>
    <div class="faq-item"><div class="faq-q">Q12: 重開機後藍牙自動開啟？</div><div class="faq-a">這是 iOS 預設行為，請務必從「設定」頁面手動關閉。</div></div>
    <div class="faq-item"><div class="faq-q">Q13: 無法解鎖？</div><div class="faq-a">確認 MDM 位置權限設為「永遠」且開啟「精確位置」。</div></div>
    <div class="faq-item"><div class="faq-q">Q14: 上鎖狀態更新 iOS？</div><div class="faq-a">強烈不建議，易導致系統錯亂。</div></div>
    <div class="faq-item"><div class="faq-q">Q15: UUID 不是唯一？</div><div class="faq-a">請檢查並清理手機儲存空間。</div></div>
    <div class="faq-item"><div class="faq-q">Q16: MDM 閃退排查？</div><div class="faq-a">請檢查企業級憑證信任狀態，確認憑證未過期。</div></div>
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
