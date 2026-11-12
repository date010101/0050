# 聆鈴五零

按下門鈴，先聽，再看。收錄台灣日常聲音的互動網站。

## 檔案
- `index.html`：整個網站，介紹頁、巷子、門口、影像頁都在這一個檔案
- `videos/`：放影片的資料夾
- `.github/copilot-instructions.md`：給 GitHub Copilot 的專案說明，讓它用繁體中文、用初學者聽得懂的方式回答

## 一、放上 GitHub（不用打指令）
1. 登入 GitHub，右上角「+」→ **New repository**，名稱例如 `linglin50`，選 **Public**，按 **Create repository**
2. 在新專案頁面點 **uploading an existing file**，把這個資料夾裡的所有東西拖進去，按 **Commit changes**
   - `.github` 是隱藏資料夾：Mac 在 Finder 按 `Cmd + Shift + .` 才看得到；Windows 在檔案總管「檢視」勾選「隱藏的項目」
   - 如果網頁上傳漏掉 `.github`，可以之後用 GitHub Desktop 上傳
3. 進入 **Settings → Pages**，Source 選 **Deploy from a branch**，Branch 選 `main`、資料夾選 `/ (root)`，按 **Save**
4. 等一兩分鐘，Pages 頁面上方會出現網址：`https://你的帳號.github.io/linglin50/`

## 二、放影片
- 影片放進 `videos` 資料夾，檔名跟住戶名稱一模一樣，例如 `videos/剁魚.mp4`
- 網站打開時會自動把影片住進那一戶
- 規格與容量限制見 `videos/README.md`

## 三、用 VS Code 和 Copilot 修改
1. 安裝 **VS Code**、VS Code 裡的 **GitHub Copilot** 擴充功能，以及 **GitHub Desktop**
2. GitHub Desktop：File → Clone repository → 選 `linglin50`，下載到電腦
3. 用 VS Code 打開這個資料夾
4. 預覽：安裝 **Live Server** 擴充功能，在 `index.html` 按右鍵選 **Open with Live Server**
   - 直接雙擊打開 `index.html` 也能看，但 `videos` 資料夾的影片不會自動載入
5. 打開 Copilot 聊天，用中文說要改什麼（範例見下方），一次改一件事
6. 確認沒問題後，到 GitHub Desktop 寫一句修改說明 → **Commit to main** → **Push origin**，一兩分鐘後網站就會更新
7. 改壞了：GitHub Desktop 的 History 可以看到每一次的修改，在要撤銷的那一筆按右鍵選 **Revert changes in commit**

## 給 Copilot 的指令範例
- 「把巷子房子的招牌改成直立式，像台灣老街的直招牌」
- 「先聽的秒數預設從 2 秒改成 3 秒」
- 「在資料欄加一個『使用語言』的欄位」
- 「把介紹頁的前言改成下面這段文字：……」
- 「手機版的巷子改成一排只放一戶」
- 「把海棠花玻璃的模糊程度調低一點，讓影像更看得出輪廓」
- 「這段錯誤訊息是什麼意思，要怎麼修？」（把錯誤訊息整段貼上）

## 用指令列（進階，可略過）
```
git clone https://github.com/你的帳號/linglin50.git
cd linglin50
git add .
git commit -m "修改說明"
git push
```
