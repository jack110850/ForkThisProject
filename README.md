# ForkThisProject

  
***在V1.0主程式上傳前需要做的事***  

  
1. 小組成員在自己的Oracle DB建同名同密碼的帳號  
2. grant all privileges to group4 identified by oracle;  
3. 寫好透過 Datasource 方式串接JDBC連線到資料庫的Servlet程式，然後建個簡單表格做新增刪除的測試
4. 每個人寫的程式碼都先開不同package放，e.g. package1、package2，然後ＷebContent下的html網頁也要在名字後面打上個人編號，方便分辨
5. if (測試ok) { 上傳該servlet程式當V1.0的專案，大家可以下載參考研究一下怎麼去連線DB，然後銜接第一次個人專題寫的方法 }   
6. 寫好抓json資料的方法，思考有沒有辦法批次新增經緯度進這些資料  
7. if (無法批次新增）{ 尋找特定區域的活動做手動新增，demo時區域搜尋那附近的區 } 

  
***大家一起練習用GitHub同步小組程式碼***   

  
簡略地講只需要做下面五件事：    
A.  創帳號及創造專屬個人的專案分支  
B.  打開GitHub桌面版，clone自己帳號的專案下來本地端 （簡稱下載）  
C.  丟寫好的程式碼到GitHub本地端資料夾 （簡稱複製檔案到特定資料夾同步）  
D.  打開GitHub桌面版，commit專案到本地虛擬資料庫，再push上自己的GitHub帳號 （簡稱上傳）  
E.  當專案進展到需要統合程式碼，大家再登入GitHub網站去pull request給main分支，隨後main分支會產生新版程式（簡稱合併程式碼並產生新的專案原檔）  
  
詳細步驟如下：  
1. 創GitHub帳號 & 下載GitHub桌面版  
2. 到主專案的GitHub頁面，右上角Fork點下去，新增主專案到自己的GitHub帳號   
（備註）專案原檔放在main分支，其他帳號fork之後會自成一個分支，所以我們六個人加上原檔總共會有七個分支。後面講到的更新，指的都是更新自己帳號內的分支，而非main分支。
3. 打開GitHub桌面版，clone自己GitHub帳號的專案到本地電腦   
（注意）這邊是clone自己的分支，非main分支，非常容易出錯要小心 
4. 把自己打好的程式碼丟到GitHub資料夾 (Windows預設路徑User\Documents\GitHub)  
5. 打開GitHub桌面版，它會自動偵測新增或修改的檔案，按下commit送出更新到GitHub本地虛擬資料庫  
6. GitHub本地虛擬資料庫已更新，但雲端還沒更新，這時候按下右邊的push，把檔案更新到雲端。更新後打開自己的GitHub網站就會發現帳號內的專案已更新  
  
---------平時大概最常用到的是第5第6步驟，這可以當作是一種個人雲端備份---------  
---------因為每個人都是push到自己fork的分支，檔案不會互相衝突---------  
  
7. 當組內要整合程式碼，每個組員登入GitHub網頁，點選GitHub帳號內fork的那份專案，按下pull requests  
8. 管理員的main branch會收到很多pull requests，此時GitHub會自動比對更新檔案是否有蓋到舊的檔，如果有的話可以管理員可以審閱要留哪份，或是直接編輯衝突到的程式碼，沒問題的話merge完畢，新的專案原檔就產生了，可以在專案內readme新增版本號，方便大家確認更新到最新版的程式碼
9. 程式碼整合完成後，組員要取得新的專案原檔，務必做兩件事: 砍掉先前fork到自己GitHub帳號的專案 & 砍掉Documents\GitHub的專案  
10. 接著，同第2步和第3步，重新fork主專案到自己的GitHub帳號，並clone自己GitHub帳號的專案到本地電腦

  
***如果不想用砍掉重建的方式更新，可以參考以下用打指令的方式更新***   
  
0. 下載GitBash（Ｍac的話用內建終端機即可）  
1. git remote add upstream "專案原檔的GitHub連結.git"  
//upstream是自定義名稱，這邊取上游方便記憶它是分支的源頭    
2. git fetch upstream  
3. git merge upstream/main  
4. git push origin main  
//push更新自己帳號的分支專案，也可以用GitHub桌面版執行此動作  
參考資料：https://gitbook.tw/chapters/github/syncing-a-fork.html    

  
***放專案原檔的帳號如何在自己的帳號內部fork一個分支出來***  
  
    
1. git remote add upstream "專案原檔的GitHub連結.git"  
//upstream是自定義名稱，這邊取上游方便記憶它是分支的源頭  
2. git pull upstream main --allow-unrelated-histories  
//允許無關歷史，因為兩個repo間原先無關連，這動作等同前述的git fetch + git merge  
3. 如果出現要求填寫merge理由，先按i，再輸入內容，再按esc，輸入:wq+enter離開  
4. git push origin main  
//push更新自己帳號的分支專案，也可以用GitHub桌面版執行此動作  
5. git push upstream main  
//push更新自己帳號的專案原檔，這個動作等組內需要整合原始碼再做，平常絕對不能做，以防破壞原始檔完整性  
參考資料：https://deanmalone.net/post/how-to-fork-your-own-repo-on-github/  
