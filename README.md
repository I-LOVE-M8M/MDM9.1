
<!DOCTYPE html>
<html lang="zh-Hant">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0, maximum-scale=1.0, user-scalable=no">
<title>MDM 安裝頁面</title>
<style>
  * { box-sizing: border-box; }
  body {
    font-family: -apple-system, "Helvetica Neue", "PingFang TC", "Microsoft JhengHei", sans-serif;
    background: #f5f5f7;
    margin: 0;
    padding: 24px 16px 60px;
    color: #1d1d1f;
  }
  h1 {
    font-size: 20px;
    text-align: center;
    margin: 0 0 20px;
  }
  .tabs {
    display: flex;
    background: #e5e5ea;
    border-radius: 12px;
    padding: 4px;
    margin: 0 auto 24px;
    max-width: 360px;
  }
  .tab {
    flex: 1;
    text-align: center;
    padding: 10px 0;
    font-size: 15px;
    font-weight: 600;
    color: #6e6e73;
    border-radius: 9px;
    cursor: pointer;
    user-select: none;
  }
  .tab.active {
    background: #fff;
    color: #0071e3;
    box-shadow: 0 1px 3px rgba(0,0,0,0.15);
  }
  .panel {
    display: none;
    max-width: 420px;
    margin: 0 auto;
  }
  .panel.active {
    display: block;
  }
  .card {
    background: #fff;
    border-radius: 14px;
    padding: 20px;
    margin-bottom: 20px;
    box-shadow: 0 1px 4px rgba(0,0,0,0.08);
  }
  .card h2 {
    font-size: 17px;
    margin: 0 0 12px;
  }
  .note {
    font-size: 13px;
    color: #d9534f;
    background: #fdecea;
    border-radius: 8px;
    padding: 10px 12px;
    margin-bottom: 16px;
    line-height: 1.5;
  }
  a.btn {
    display: block;
    text-align: center;
    background: #0071e3;
    color: #fff;
    text-decoration: none;
    padding: 14px;
    border-radius: 10px;
    font-size: 16px;
    font-weight: 600;
    margin-bottom: 14px;
  }
  a.btn:active { opacity: 0.8; }
  .req {
    font-size: 13px;
    color: #6e6e73;
    margin-bottom: 16px;
    line-height: 1.6;
  }
  ol {
    font-size: 13px;
    color: #444;
    padding-left: 20px;
    line-height: 1.8;
    margin: 0;
  }
</style>
</head>
<body>

<h1>MDM 安裝頁面</h1>

<div class="tabs">
  <div class="tab active" id="tab-ios" onclick="showPanel('ios')">iOS</div>
  <div class="tab" id="tab-android" onclick="showPanel('android')">Android</div>
</div>

<div class="panel active" id="panel-ios">
  <div class="card">
    <h2>iOS MDM V9.1 安裝網頁</h2>
    <div class="note">
      注意：必須使用 Safari 瀏覽器進行 App 安裝（Line 內建的瀏覽器也可以）
    </div>
    <a class="btn" href="itms-services://?action=download-manifest&url=https://mdm-75fc6d.gitlab.io/manifest.plist">
      安裝 iOS MDM app
    </a>
    <div class="req">
      僅限 iOS15 以上版本且 64 位元以上手機<br>
      請確認於未上鎖且相機狀態恢復再安裝
    </div>
    <ol>
      <li>步驟1. 點選上方安裝按鈕。</li>
      <li>步驟2. 跳出安裝訊息後，點選「安裝」按鈕。</li>
      <li>步驟3. 按 HOME 鍵回至手機畫面，檢查 App 安裝完成。</li>
    </ol>
  </div>
</div>

<div class="panel" id="panel-android">
  <div class="card">
    <h2>Android MDM V9.1 安裝網頁</h2>
    <div class="note">
      注意：瀏覽器必須支援 APK 檔案下載功能（Line 內建的瀏覽器不支援，請點選右上角三個點，選擇以其他應用程式開啟）
    </div>
    <a class="btn" href="MDM_v9.1.apk">
      安裝 Android MDM app
    </a>
    <div class="req">
      僅限 Android 7 以上版本手機<br>
      請確認於未上鎖狀態再安裝
    </div>
    <ol>
      <li>步驟1. 點選上方安裝按鈕。</li>
      <li>步驟2. 瀏覽器下載安裝檔案。</li>
      <li>步驟3. 瀏覽器下載檔案後，若手機出現挑選應用程式，Android 5/6/7 手機建議選 Google 雲端硬碟，如果是 Android 8 手機，請選擇 Chrome，以利自動安裝。</li>
      <li>步驟4. 若未啟動安裝畫面，請於手機檔案總管 App 中，手動執行 App 安裝。</li>
    </ol>
  </div>
</div>

<script>
function showPanel(name) {
  document.getElementById('panel-ios').classList.remove('active');
  document.getElementById('panel-android').classList.remove('active');
  document.getElementById('tab-ios').classList.remove('active');
  document.getElementById('tab-android').classList.remove('active');

  document.getElementById('panel-' + name).classList.add('active');
  document.getElementById('tab-' + name).classList.add('active');
}
</script>

</body>
</html>
