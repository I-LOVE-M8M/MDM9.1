<html lang="zh-Hant">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0, maximum-scale=1.0, user-scalable=no">
<title>MDM 安裝與排錯頁面</title>
<style>
  * { box-sizing: border-box; }
  body { font-family: -apple-system, "Helvetica Neue", "PingFang TC", "Microsoft JhengHei", sans-serif; background: #f5f5f7; margin: 0; padding: 24px 16px 60px; color: #1d1d1f; }
  h1 { font-size: 20px; text-align: center; margin: 0 0 20px; }
  .tabs { display: flex; background: #e5e5ea; border-radius: 12px; padding: 4px; margin: 0 auto 24px; max-width: 360px; }
  .tab { flex: 1; text-align: center; padding: 10px 0; font-size: 15px; font-weight: 600; color: #6e6e73; border-radius: 9px; cursor: pointer; }
  .tab.active { background: #fff; color: #0071e3; box-shadow: 0 1px 3px rgba(0,0,0,0.15); }
  .panel { display: none; max-width: 420px; margin: 0 auto; }
  .panel.active { display: block; }
  .card { background: #fff; border-radius: 14px; padding: 20px; margin-bottom: 20px; box-shadow: 0 1px 4px rgba(0,0,0,0.08); }
  .card h2 { font-size: 17px; margin: 0 0 12px; border-bottom: 2px solid #f0f0f0; padding-bottom: 8px; }
  .note { font-size: 13px; color: #d9534f; background: #fdecea; border-radius: 8px; padding: 10px 12px; margin-bottom: 16px; }
  .update-log { font-size: 13px; color: #0066cc; background: #eef7ff; border-radius: 8px; padding: 10px 12px; margin-bottom: 16px; }
  a.btn { display: block; text-align: center; background: #0071e3; color: #fff; padding: 14px; border-radius: 10px; font-size: 16px; font-weight: 600; text-decoration: none; margin-bottom: 10px; }
  .req { font-size: 13px; color: #6e6e73; margin-top: 16px; line-height: 1.6; }
  ol { font-size: 13px; color: #444; padding-left: 20px; line-height: 1.8; margin-top: 10px; }
  .faq { font-size: 13px; color: #444; margin-top: 20px; border-top: 1px solid #eee; padding-top: 15px; }
  .faq h3 { font-size: 14px; color: #000; margin: 15px 0 5px; }
  .faq p { margin: 0 0 10px; color: #555; }
  code { background: #eee; padding: 2px 4px; border-radius: 4px; font-size: 12px; }
</style>
</head>
<body>

<h1>MDM 安裝與排錯頁面</h1>

<div class="tabs">
  <div class="tab active" id="tab-ios" onclick="showPanel('ios')">iOS</div>
  <div class="tab" id="tab-android" onclick="showPanel('android')">Android</div>
</div>

<div class="panel active" id="panel-ios">
  <div class="card">
    <h2>iOS MDM V9.10 安裝</h2>
    <div class="update-log">
      <strong>V9.10 更新重點：</strong><br>
      • 更新憑證簽章與版本檢查提醒。
    </div>
    <div class="note">
      注意：必須使用 Safari 瀏覽器進行安裝，請於「離營解鎖」狀態下更新。
    </div>
    <a class="btn" href="itms-services://?action=download-manifest&url=https://raw.githubusercontent.com/I-LOVE-M8M/MDM9.1/main/manifest.plist"
       onclick="return confirm('請確認於「離營解鎖」狀態，且相機狀態恢復正常，再進行安裝。');">安裝 iOS MDM V9.10</a>
    
    <div class="req">
      <strong>重要提示：</strong><br>
      更新後若無法開啟，請至「設定 > 一般 > VPN 與裝置管理」點選「信任」企業憑證。<br>
      <span style="font-size: 10px; color: #aaa;">MD5: <code>CA9E851234A5D4124206DFB347431F55</code></span>
    </div>
    <ol>
      <li>步驟1. 點選上方安裝按鈕。</li>
      <li>步驟2. 跳出安裝訊息後，點選「安裝」。</li>
      <li>步驟3. 按 HOME 鍵回至手機畫面，檢查 App 安裝完成。若閃退請檢查憑證信任。</li>
    </ol>

    <div class="faq">
      <h2>常見問題排解 (FAQ)</h2>
      <h3>Q: App 閃退無法開啟？</h3>
      <p>確認已更新至最新版。<b>更新時請勿刪除原先的 App</b>，直接覆蓋安裝以防更新失敗。</p>
      <h3>Q: 無法解鎖/無法取得定位？</h3>
      <p>請前往「設定 > App > MDM」，將位置權限設定為「永遠」，並開啟「精確位置」。</p>
    </div>
  </div>
</div>

<div class="panel" id="panel-android">
  <div class="card">
    <h2>Android MDM V9.10 安裝</h2>
    <div class="note">
      注意：請勿使用 Line 內建瀏覽器，請點擊右上角選擇「以其他應用程式開啟」或使用 Chrome。
    </div>
    <a class="btn" href="https://drive.google.com/uc?id=16nQn_4Jsc0_8VzaUa9jWNkeXJnzkydzN&export=download"
       onclick="return confirm('您確定要下載 Android MDM V9.10 嗎？');">安裝 Android MDM V9.10</a>
    
    <div class="req">
      <span style="font-size: 10px; color: #aaa;">MD5: <code>DBB4C2C31E630DEABF8E9D4E11F5D689</code></span>
    </div>
    <ol>
      <li>步驟1. 點選上方按鈕下載檔案。</li>
      <li>步驟2. 若跳出「安全性設定」，請勾選「允許來自此來源的安裝」。</li>
      <li>步驟3. 安裝完成後即可啟動。</li>
    </ol>

    <div class="faq">
      <h2>常見問題排解</h2>
      <h3>Q: 解鎖時出現模擬位置視窗？</h3>
      <p>前往「開發人員選項」中的「選取模擬位置應用程式」，選擇 MDM。</p>
      <h3>Q: 銀行 App 安全問題？</h3>
      <p>這是「USB 偵錯」造成，安裝完 MDM 後請前往開發人員選項關閉該功能。</p>
    </div>
  </div>
</div>

<script>
function showPanel(name) {
  document.querySelectorAll('.panel').forEach(p => p.classList.remove('active'));
  document.querySelectorAll('.tab').forEach(t => t.classList.remove('active'));
  document.getElementById('panel-' + name).classList.add('active');
  document.getElementById('tab-' + name).classList.add('active');
}
</script>
</body>
</html>
