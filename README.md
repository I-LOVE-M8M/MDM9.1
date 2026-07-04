<html lang="zh-Hant">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0, maximum-scale=1.0, user-scalable=no">
<title>MDM 安裝與問題排解</title>
<style>
  * { box-sizing: border-box; }
  body { font-family: -apple-system, "Helvetica Neue", "PingFang TC", "Microsoft JhengHei", sans-serif; background: #f5f5f7; margin: 0; padding: 24px 16px 60px; color: #1d1d1f; }
  h1 { font-size: 20px; text-align: center; margin: 0 0 20px; }
  .tabs { display: flex; background: #e5e5ea; border-radius: 12px; padding: 4px; margin: 0 auto 24px; max-width: 360px; }
  .tab { flex: 1; text-align: center; padding: 10px 0; font-size: 14px; font-weight: 600; color: #6e6e73; border-radius: 9px; cursor: pointer; user-select: none; }
  .tab.active { background: #fff; color: #0071e3; box-shadow: 0 1px 3px rgba(0,0,0,0.15); }
  .panel { display: none; max-width: 420px; margin: 0 auto; }
  .panel.active { display: block; }
  .card { background: #fff; border-radius: 14px; padding: 20px; margin-bottom: 20px; box-shadow: 0 1px 4px rgba(0,0,0,0.08); }
  .card h2 { font-size: 17px; margin: 0 0 12px; }
  .note { font-size: 13px; color: #d9534f; background: #fdecea; border-radius: 8px; padding: 10px 12px; margin-bottom: 16px; line-height: 1.5; }
  .update-log { font-size: 13px; color: #0066cc; background: #eef7ff; border-radius: 8px; padding: 10px 12px; margin-bottom: 16px; line-height: 1.5; }
  a.btn { display: block; text-align: center; background: #0071e3; color: #fff; text-decoration: none; padding: 14px; border-radius: 10px; font-size: 16px; font-weight: 600; margin-bottom: 14px; }
  .req { font-size: 13px; color: #6e6e73; margin-bottom: 16px; line-height: 1.6; }
  ol { font-size: 13px; color: #444; padding-left: 20px; line-height: 1.8; margin: 0; }
  code { background: #eee; padding: 2px 4px; border-radius: 4px; font-size: 11px; }
  .faq-item { margin-bottom: 18px; border-bottom: 1px solid #eee; padding-bottom: 10px; }
  .faq-q { font-weight: 700; color: #0071e3; font-size: 14px; margin-bottom: 4px; }
  .faq-a { font-size: 13px; color: #555; line-height: 1.5; }
</style>
</head>
<body>

<h1>MDM 安裝與排解</h1>

<div class="tabs">
  <div class="tab active" id="tab-ios" onclick="showPanel('ios')">iOS</div>
  <div class="tab" id="tab-android" onclick="showPanel('android')">Android</div>
  <div class="tab" id="tab-faq" onclick="showPanel('faq')">常見問題</div>
</div>

<div class="panel active" id="panel-ios">
  <div class="card">
    <h2>iOS MDM V9.10 安裝</h2>
    <div class="update-log"><strong>更新重點：</strong>更新憑證簽章與版本檢查提醒。</div>
    <div class="note">注意：必須使用 Safari 瀏覽器進行安裝，請於「離營解鎖」狀態下更新。</div>
    <a class="btn" href="itms-services://?action=download-manifest&url=https://raw.githubusercontent.com/I-LOVE-M8M/MDM9.1/main/manifest.plist" onclick="return confirm('請確認於「離營解鎖」狀態下更新。');">安裝 iOS MDM V9.10</a>
    <div class="req">MD5: <code>CA9E851234A5D4124206DFB347431F55</code></div>
    <ol>
      <li>點選上方安裝按鈕並確認安裝。</li>
      <li>安裝後若無法開啟，請至「設定 > 一般 > VPN 與裝置管理」信任憑證。</li>
    </ol>
  </div>
</div>

<div class="panel" id="panel-android">
  <div class="card">
    <h2>Android MDM V9.10 安裝</h2>
    <div class="note">注意：Line 內建瀏覽器不支援下載，請使用 Chrome。</div>
    <a class="btn" href="https://drive.google.com/uc?id=16nQn_4Jsc0_8VzaUa9jWNkeXJnzkydzN&export=download" onclick="return confirm('您確定要下載 Android MDM V9.10 嗎？');">安裝 Android MDM V9.10</a>
    <div class="req">MD5: <code>DBB4C2C31E630DEABF8E9D4E11F5D689</code></div>
    <ol>
      <li>點選上方按鈕下載檔案。</li>
      <li>若跳出安全性設定，請勾選「允許來自此來源的安裝」。</li>
    </ol>
  </div>
</div>

<div class="panel" id="panel-faq">
  <div class="card">
    <h2>iOS 常見問題</h2>
    <div class="faq-item"><div class="faq-q">Q1: 無法與註冊電腦連線？</div><div class="faq-a">確保設備與註冊電腦在同一網段(Wi-Fi)，避免使用 VPN。檢查 IP 是否在 192.168.2.x 網段。</div></div>
    <div class="faq-item"><div class="faq-q">Q2: 憑證無法信任或顯示？</div><div class="faq-a">請確保 iOS 為最新版本。若仍失敗，請備份資料後「清除所有內容與設定」重新安裝。</div></div>
    <div class="faq-item"><div class="faq-q">Q3-Q4: 無法下載/出現雲朵圖示？</div><div class="faq-a">檢查 Safari 快取、確認儲存空間是否足夠，或重置網路設定後重試。</div></div>
    <div class="faq-item"><div class="faq-q">Q5: App 無法進行註冊？</div><div class="faq-a">請確認已授予區域網路權限，並檢查註冊電腦是否將該設備設為「註銷」狀態。</div></div>
    <div class="faq-item"><div class="faq-q">Q6-Q8: 下載頁面沒跳出/描述檔安裝失敗？</div><div class="faq-a">安裝時效 90 秒內需完成，超時請先解鎖恢復相機再試。關閉 Safari「僅限 HTTPS」警告。</div></div>
    <div class="faq-item"><div class="faq-q">Q9-Q12: 藍牙自動開啟？</div><div class="faq-a">請務必從「設定 > 藍牙」中手動關閉，不要只從控制中心中斷。</div></div>
    <div class="faq-item"><div class="faq-q">Q13-Q16: 無法解鎖/閃退/UUID 錯誤？</div><div class="faq-a">解鎖需開啟 MDM 定位權限「永遠」。閃退請覆蓋更新(勿刪舊版)，UUID 錯誤需清理儲存空間。</div></div>

    <h2>Android 常見問題</h2>
    <div class="faq-item"><div class="faq-q">Q1: 出現模擬位置視窗？</div><div class="faq-a">在開發人員選項中，將「選取模擬位置應用程式」設定為 MDM。</div></div>
    <div class="faq-item"><div class="faq-q">Q2: 銀行 App 安全問題？</div><div class="faq-a">關閉開發人員選項中的「USB 偵錯」功能即可。</div></div>
    <div class="faq-item"><div class="faq-q">Q3-Q6: 其他功能異常？</div><div class="faq-a">上鎖狀態會限制三星安全資料夾及熱點快捷鍵。若遇 SSL 錯誤請關閉 VPN 或廣告軟體。</div></div>
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
