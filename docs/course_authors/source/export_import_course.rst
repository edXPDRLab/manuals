 
*************************
匯出或匯入課程
*************************
 
Studio有一個匯入工具以及一個匯出工具如此你可以用以匯入匯出課程。

 
匯出一個課程
***************
 
你可以將一個已在Studio裡創建的課程匯出。 你可以匯出一個課程來
讓另一個instructor使用，或是用來備份你的課程。
 
 
例如，你在Studio中創建一個課程，並且run此課程。 
一個朋友或是同事，包括來自另一institution的朋友，可能有興趣於
running他們自己客製化後的課程。 
你能將你創建的課程匯出並將其給予其他nstructor。
此instructor接著就可匯入此課程，做任何修改以符合其instructor的情況，
並將課程發佈給學生。
 
 
或者，你可以匯出你的課程，並在Studio做任何修改。
若你之後想將課程改回先前的版本，
你可以匯入你匯出的版本。注意若你做此動作時課程仍在running，
將遺失你的學生的work.
 
 
當你匯出你的課程，Studio會創建一個**.tar.gz**檔案其中包含
以下課程資料:
 
 
1. 課程結構 (sections及subsections的順序)
 
 
2. 個別的units
 
 
3. 個別的problems
 
 
4. Additional pages
 
 
5. Files & Uploads 頁面中的檔案
 

 
匯出的檔案不會包含以下資料:
 
 
1. 學生或使用者資料
 
 
2. Discussion forum data
 
 
3. 課程設定
 
 
4. Certificates
 
 
5. Grading information


.. raw:: latex
  
      \newpage %
 

匯入課程
***************


 
.. warning::

	請小心使用此功能!
	匯入一個新的課程將會刪除目前所有與你課程有關聯的內容
	並以上傳的檔案中的內容取代。
	課程的匯入無法復原
 
 
你可以匯入一個已存在於Studio的課程。 These can
be courses that you or someone else has created and exported.
 
 
你匯入的檔案必須是一個**.tar.gz**檔案其中包含，至少，
一個Course.xml檔案位於課程資料目錄。 此tar.gz檔必須要
與課程資料目錄命名相同
 
 
若你的課程使用legacy layout structures，你將不能在Studio中編輯你的課程
，即使其會正確地在Edge裡顯示，要確定你的課程是完全可編輯的，
確定你所有的教材都被嵌入一個unit。
 
 
匯入一個課程:
 
 
1. 在navigation bar，點擊**Tools**，接著點擊**Import**。
 
 
.. image:: Images/image243.png
 
 
2. 在**Course to Import**下方，點擊**Choose File**。
 
 
3. 找到你要的檔案，接著點擊**Open**。

