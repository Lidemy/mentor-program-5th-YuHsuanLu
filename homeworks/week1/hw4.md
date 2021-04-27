## 跟你朋友介紹 Git
Git是版本控制的軟體，，可用於多人協作時控制檔案版本

### 下載完 Git 可以開始讓 Git 管理指定路徑的資料夾之版本控制
`git init` 讓Git開始(initialize)管理指定路徑的資料夾的指令

### 把修改後的檔案加入檔案庫有2個步驟
1. `git add` 指令把檔案加入Git索引（`git add` 決定是否加入版本控制）
2. `git commit` 把Git 索引中的檔案加入檔案庫（`git commit`新建一個版本）
add & commit 的概念有點像買衣服，把確定會買的衣服放在櫃台，跟店員說先幫我留著（add）；最後都確定之後，一起結帳（commit）。

### `git commit -am "message"` 一次完成 add + commit
- 比起 `m` ，多一個 `a` 就可以讓兩個動作add+commit一次完成
- 建議每次都輸入 `git commit -am "message"` 當成習慣，以免忘記 `add` 
- 這裡要小心留意回報的訊息，如果出現 “no changes added to commit”，代表可能有新增的檔案忘記 `add`，根據 [Git 官網文件](https://git-scm.com/docs/git-commit)， `-a` 不適用於新增的檔案，所以如果有新檔案的加入，還是得先 `add` 再 `commit`。
    Tell the command to automatically stage files that have been modified and deleted, but new files you have not told Git about are not affected.

### `git status`
檢視路徑中的版本控制狀態

### 分支 branch
需要在分支branch操作情況: 多人協作不同功能
- `git branch` 不給任何參數直接執行此命令的話，會顯示分支列表
- `git branch <branch-name>` 通過此命令來建立分支
- `git checkout <branch-name>`通過此命令來切換到branch-name的分支
- `git checkout -b <branch-name>` 直接開branch+切到該branch

### push 和 pull
`push`： 推上 repository，同步到 GitHub 上面
- `git push original <branh-name>`

`pull`： 從 repository 拉下來，從 GitHub 同步回到本地
- `git pull original <branh-name>`