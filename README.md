# ForkThisProject
大家一起來練習建立GitHub雲端，步驟如下: 
  
1. 創GitHub帳號 & 下載GitHub桌面版  
2. 到主專案的GitHub頁面，右上角Fork點下去，新增主專案到自己的GitHub帳號  
2.1. 主專案是master分支，其他帳號fork之後也會自成一個分支，所以我們六個人共會有七個分支，master分支直到程式碼整合後才會更新，  
3. 打開GitHub桌面版，clone自己GitHub帳號的專案到本地電腦 (注意，這邊是clone自己的分支，非master分支)  
4. 把自己打好的程式碼丟到Documents\GitHub (window預設路徑)  
5. 打開GitHub桌面版，它會自動偵測新增或修改的檔案，按下commit送出更新到GitHub本地資料庫  
6. GitHub本地資料庫已更新，但雲端還沒，這時候按下右邊的push，把本地資料庫檔案更新到雲端，更新後再打開自己的GitHub就會發現帳號內的專案資料更新了
  
---------平時大概最常用到的是第5第6步驟，這可以當作是一種個人雲端備份，因為每個人都是push到自己fork的分支，不會互相衝突---------
---------整合程式碼後專案名稱會加V1.0之類的後綴詞防止和舊檔混淆---------
  
7. 當組內要整合程式碼時，每個組員登入GitHub，選擇GitHub帳號內fork的那個專案，按下pull requests  
8. 管理員的master branch會收到很多pull requests，此時GitHub會自動比對更新檔案是否有蓋到舊的檔，如果有的話可以管理員可以審閱要留哪份，或是直接編輯衝突到的程式碼  
9. 程式碼整合完成後，組員要更新最新版的程式碼，必須做兩件事: 砍掉先前fork到自己GitHub帳號的專案 & 砍掉Documents\GitHub的專案  
10. 從第2步開始，重新fork主專案到自己的GitHub帳號並下載到本地電腦
