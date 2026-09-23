![GitHub 入門教學 ，一招半式闖GitHub](https://raw.githubusercontent.com/jangowlong/MyFirstRepository/db9c94446103e2ad048859f3a3cdea38f24ff51a/img/GitHub%20%E5%85%A5%E9%96%80%E6%95%99%E5%AD%B8%20%EF%BC%8C%E4%B8%80%E6%8B%9B%E5%8D%8A%E5%BC%8F%E9%97%96GitHub.jpg)

# GitHub 入門教學 ，一招半式闖GitHub

#### GitHub 是全球最大代碼託管平台，免費帳號已足夠個人項目使用。本文由建立帳號、Git 基本操作、第一個 Commit 到 GitHub Pages 免費建站，帶你完全入門。

![img](https://raw.githubusercontent.com/jangowlong/MyFirstRepository/e8a672d2c49d9dbf15841f091b3c3fc8a55d3b06/img/%E6%B7%BA%E7%B6%A0%E7%B7%9A001-1024x11.jpg)

#### GitHub 免費帳號支援無限 Public Repository，建立帳號後裝 Git（git-scm.com），輸入 `git init`、`git add .`、`git commit`、`git push` 四條指令即完成第一次上傳。

#### 其實 Git + GitHub 是業界標準，而且完全免費入門。這篇文章由零開始，帶你完成由裝 Git 到第一次 push 代碼，以及用 GitHub Pages 免費建靜態網站，全程無需要信用卡。

## GitHub 是什麼？了解開發者必用？

#### **GitHub** 是一個雲端代碼託管平台，底層技術是 **Git**——一個版本控制系統。兩者分別：

- **Git**：本地工具，追蹤代碼修改歷史，讓你可以回到任何一個舊版本
- **GitHub**：雲端平台，把 Git 倉庫（Repository）同步上網，方便備份、分享、協作

#### GitHub 免費版可以做嗎?：

- 無限 Public Repository（公開項目）
- 無限 Private Repository（私人項目，2019 年起免費開放）
- GitHub Pages（免費靜態網站託管）
- GitHub Actions（自動化 CI/CD，每月 2,000 分鐘免費）
- GitHub Copilot（AI 代碼補全，學生及部分用家免費）

#### 全球超過 1 億開發者用 GitHub，幾乎所有 open source 項目都使用。學會 GitHub 是進入開發者圈子的基本門票。

## 建立帳號同基本設定

#### **Step 1：建立 GitHub 帳號**

1. 去 [github.com](https://github.com/)，點右上角 “Sign up”
2. 填電郵、密碼、用戶名（Username 一旦設定後，是你的永久 URL：`github.com/你的用戶名`，謹慎選擇）
3. 完成驗證，選 Free 方案

#### **Step 2：安裝 Git 本地工具**

#### Windows：

- 去 [git-scm.com/download/win](https://git-scm.com/download/win) 下載安裝程式
- 安裝時保持預設選項即可
- 安裝完後打開「Git Bash」（已安裝）

#### macOS：

- 打開 Terminal，輸入 `git --version`
- 如果未裝，系統會提示安裝 Xcode Command Line Tools，跟指示做

#### **Step 3：設定用戶資訊（只需做一次）**

```
git config --global user.name "你的名字"
git config --global user.email "你的電郵@example.com"
```

#### 這個設定決定每次 commit 顯示的名字，設定完就無需要每次重設。

## Git 基本指令教學（init / add / commit / push / pull）

#### 以下是最常用的 Git 指令，學會這 6 個已足夠日常使用：

#### **初始化本地倉庫：**

```
git init
```

#### 在你的項目資料夾裡面執行，這會建立 `.git` 隱藏資料夾，代表這個資料夾是 Git 倉庫。

#### **查看目前狀態：**

```
git status
```

#### 顯示有無未儲存的修改、有無新文件未被追蹤。養成每次操作前先 `git status` 這習慣。

#### **添加文件到暫存區：**

```
git add .          # 添加所有改動
git add index.html # 只添加指定文件
```

#### **提交改動（建立 Commit）：**

```
git commit -m "描述這次做什麼改動"
```

#### 引號裡面寫清楚改動內容，例如 “Add homepage design” 或 “Fix login bug”，方便之後回看。

#### **連接 GitHub 遠端倉庫：** 先在 GitHub 新建一個 Repository（點右上角 `+` → New repository），然後：

```
git remote add origin https://github.com/你的用戶名/你的項目名.git
git branch -M main
git push -u origin main
```

#### **之後每次更新代碼：**

```
git add .
git commit -m "變更改動描述"
git push
```

#### **從遠端拉取最新代碼（多裝置或協作時用）：**

```
git pull
```

------

## GitHub Pages 免費建站（5 分鐘上線靜態網頁）

#### GitHub Pages 係 GitHub 提供嘅免費靜態網站託管服務。只要你有 HTML/CSS 文件，幾分鐘就可以上線，域名格式是 `你的用戶名.github.io/項目名`。

#### **步驟：**

1. 在 GitHub 建立一個新 Repository，命名為任意名字（例如：my-website）
2. 把你的 HTML 文件 push 到該 Repository（確保有 `index.html` 在根目錄）：

```
git init
git add .
git commit -m "Initial website"
git remote add origin https://github.com/你的用戶名/my-website.git
git push -u origin main
```

1. 在 GitHub Repository 頁面，點 **Settings** → 左側 **Pages**
2. 在 “Branch” 選 `main`，資料夾選 `/ (root)`，點 Save
3. 等約 1-2 分鐘，刷新頁面後會見到 “Your site is live at `https://你的用戶名.github.io/my-website`”

#### 注意事項：

- GitHub Pages 只支援靜態內容（HTML/CSS/JS），沒有援 PHP、Python、Node.js 後端
- 免費版每月流量 100GB，每個 Repository 建議不要過 1GB
- 如需自訂域名，可在 Pages 設定裡加入，然後去域名商改 DNS 記錄

## GitHub Copilot 同 Actions 簡介（免費版有沒有）

#### **GitHub Copilot（AI 代碼補全）：** Copilot 是 GitHub 的 AI 配對程式，可以根據上文自動補全代碼、寫函數、解釋錯誤。

#### 免費版（2024 年起）：每月限制 2,000 次代碼補全 + 50 次 Chat，支援 VS Code。對於初學者已相當夠用。學生可透過 GitHub Education 申請完全免費的 Copilot Pro。

#### **GitHub Actions（自動化流程）：** Actions 是 GitHub 的 CI/CD 工具，可以設定「每次 push 後自動跑測試、自動部署」的流程。

#### 免費版每月提供 **2,000 分鐘**執行時間（Linux runner），足夠個人小項目自動部署之用。基本用法：是倉庫建立 `.github/workflows/deploy.yml` 文件，定義觸發條件同執行步驟。

#### 兩個工具對初學者來講不需要立即用，但是了解 GitHub 生態系統的重要組成部分。

## 常見問題 FAQ

#### Q1：Git 同 GitHub 是不一樣的一件事？ 不一樣 。Git 是本地安裝的版本控制工具，離線亦可使用。GitHub 是使用 Git 技術的雲端平台，用來存放同分享 Git 倉庫。除 GitHub 外，GitLab 同 Bitbucket 亦是類似平台。

#### Q2：Private Repository 真的免費嗎？ 是，GitHub 自 2019 年起，免費帳號支援無限 Private Repository。但免費 Private Repo 合作者上限是 3 人，需要更多合作者要升 Pro（$4/月）。

#### Q3：第一次 push 時要輸入密碼，了解提示有無接受？ GitHub 已於 2021 年取消密碼驗證，改為 Personal Access Token（PAT）或 SSH Key。建議用 SSH：去 GitHub Settings → SSH Keys，生成並加入本地公鑰，之後用 `git@github.com:用戶名/項目名.git` 格式連接。

#### **Q4：Commit message 用中文可以嗎？** 技術上可以，Git 支援 Unicode。但業界普遍用英文 commit message，方便跨國協作。如果是個人項目，用中文完全無問題。

#### Q5：誤刪的文件可以恢復嗎？ 只要文件曾經被 commit 過，就可以恢復。用 `git log` 查歷史，找到刪除前嘅 commit hash，用 `git checkout [hash] -- 文件路徑` 恢復指定文件。這個是 Git 最實用的嘅功能之一。
