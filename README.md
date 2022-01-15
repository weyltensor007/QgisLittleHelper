# 使用 QgisPlugin

上面所提的新增action操作, 原則上每個圖層都要手動新增, 而且無法被儲存(除非匯出qml檔), 如果一個專案有多個圖層, 這樣的處理方式就比較沒有效率。為此, 可以利用Python撰寫Qgis外掛程式, 整理使用外掛的方式如下:

1. 下載 plugin 程式檔
[下載連結](https://github.com/weyltensor007/QgisLittleHelper/blob/main/littlehelper.zip)
![](https://i.imgur.com/iYhJvAF.png)

2. 打開 QGIS 存放 plugin 的路徑
![](https://i.imgur.com/adIFjkp.png)
點選 `Open Active Profile Folder` 後, 會出現一個資料夾視窗,
![](https://i.imgur.com/dAmhljr.png)
點選 `Python`, 再點入 `plugins`, 這個地方就是等等要複製程式碼的目的地

3. 複製下載zip檔解壓縮後的資料夾到上述路徑
![](https://i.imgur.com/L6DG7bs.png)

4. 要自己微調一下照片路徑設定

    首先點進 `littlehelper` 資料夾
    ![](https://i.imgur.com/1HiUwNT.png)
    
    再點開 `python_action_scripts` 資料夾
    點2下並以編輯器開啟 `打開照片.py`, 修改 `root_dir` 變數為
    統一存放調查資料的資料夾路徑, 然後再稍微檢查一下 `glob`的層次
    ==複製完後請重新啟動QGIS==

4. 開啟 plugin 管理介面
![](https://i.imgur.com/XSpLWdX.png)

![](https://i.imgur.com/ERJRjyy.png)


5. 點選 plugin 圖示啟用功能

可以一次處理很多圖層
![](https://i.imgur.com/tcIB695.png)

點選後, 就會自動執行相關程式碼, 然後會出現下列視窗
![](https://i.imgur.com/07kUQOa.png)

這時滑鼠點選確定或者鍵盤按 `Enter` 就可以看到每個圖層都有action了!

