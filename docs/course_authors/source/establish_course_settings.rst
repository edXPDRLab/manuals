*************************
建立課程設定
*************************

新增合作者
*****************

	
    Studio支援對一個課程基本的合作編輯。使用者必須已經在studio.edge.edx.org上註冊，以及已經透過郵件的連結建立他們的帳號。如果使用者沒有找到，您將會被通知。


    在您新增一個新的使用者之前，考慮以下幾點。


    · 邀請的使用者有完整的權限可以修改您的課程，包括刪除任何人創建的課程內容。


    · 邀請的使用者目前不能在課堂上授予新權限。


    · 編輯上的衝突目前沒辦法管理。因此，課程的狀態會在頁面重新整理之後改變。


    給予其他使用者權限以修改您的課程：


    1. 在navigation bar上，點擊 **Course Settings** ，之後點擊 **Course Team** 。


    .. image:: Images/image115.png



    2. 點擊 **New User** 。


    .. image:: Images/image117.png


    3. 在 **email** 欄位，填入使用者的郵件地址，之後點擊 **Add User** 。


.. raw:: latex

      \newpage %



新增說明書Policy資料
**********************



    您可以在 **Advanced Settings** 頁面新增說明書policy資料。These advanced configuration options are specified using JSON key and value pairs.


    您只能在您非常熟悉valid configuration key value pairs以及the ways these pairs will affect your course時新增說明書policy資料。
	您頁面上的錯誤可能導致您課程發生重大的問題。
    

    edX的專案管理員可以幫助您學習有關如何應用這些設定。


    1. 在navigation bar上，點擊 **Course Settings** ，之後點擊 **Advanced Settings** 。


    2. 點擊 **New Manual Policy** .


      .. image:: Images/image119.png


    3. 在 **Policy Key** 欄位，輸入這個policy key。


    4. 在 **Policy Value** 欄位，輸入這個policy的值。


.. raw:: latex

      \newpage %


關於頁面資訊的新增
***************************


    新增一個日程安排資訊，一個敘述以及其他您課程中的資訊，使用 **Course Settings** 功能表。


     .. image:: Images/image121.png


    This takes you to the

Schedule and Details Page
=========================


1. 在這個頁面的上方，您會發現有a section with the **Basic Information** for your course。這裡您可以發現您課程的標題以及您課程可以郵寄邀請學生參加課程的URL。

 .. image:: Images/image281.png


2. 在 **Course Schedule** section，輸入您想要的開課日期在 **Course Start Date** 欄位，之後輸入您想要的開課時間在 **Course** **Start Time** 欄位。


.. note::
	
    開課時間在這畫面將會反映在您的瀏覽器中的當前時區，這取決於您的地理位置。開課時間在Edge上以UTC表示給學生看。


3. 在**Course Schedule** section，輸入您想要的課程結束日期在 **Course** **End Date** 欄位中，之後輸入您想要的課程結束時間在 **Course** **End Time** 欄位中。


新增招生資訊
==========================


1. 在 navigation bar上，點擊 **Course ** 設定，之後點擊 **Schedule & Details** 。


2. 在 **Course Schedule** section，輸入您想要開始招生的日期在 **Enrollment Start Date** 欄位，之後輸入您想要開始招生的時間在 **Enrollment Start Time** 欄位。


3. 在 **Course Schedule** section，輸入您想要結束招生的日期在 **Enrollment End Date** 欄位，之後輸入您想要結束招生的時間在 **Enrollment End Time** 欄位。


.. note::
	
    招生日期在這畫面將會反映在您的瀏覽器中的當前時區，這取決於您的地理位置。招生時間在Edge上以UTC表示給學生看。



新增課程大綱
=====================


1. 在 navigation bar上，點擊 **Course Settings**，之後點擊 **Schedule & Details** 。


2. 向下滾動到 **Introducing Your Course** section，之後找到 **Course Overview** 欄位。

.. image:: Images/image123.png




3. 在 **Course Overview** 欄位，輸入您的課程描述。


這個欄位內容是HTML格式。對於template可以使用包括placeholders，請看 :doc:`appendices/a`.



如果修您的課程中有先決條件，您可以把資訊放在課程大綱。


.. note::

    沒有儲存的按鈕。Studio會自動儲存您的改變。


接下來的是 **Course Overview** 欄位的範例內容：


.. image:: Images/image125.png

新增照片敘述
=========================

1.  選擇一個高解析度的圖片，寬度最小為660 pixels、高度最小為240 pixels。

2.  改變相片中您想要使用的檔案名稱 **images_course_image.jpg** 。

3.  上傳檔案到 **Files & Uploads** 頁面。


這張照片被命名為 **images_course_image.jpg** 自動出現在課程的About頁面上。

加入一個關於我影片
==================


您可以創建一個About video 將會出現在您課程 **About** 頁面上。


1. 上傳您想要的影片到YouTube上。請注意出現在URL中的 ** watch?v =**  和   ** &feature** 之間的編碼。這個編碼出現在綠色box之下。


.. image:: Images/image127.png


2. 在 navigation bar上，點擊 **Course Settings** ，之後點擊 **Schedule & Details** 。


3. 向下滾動到 **Introducing Your Course** section，之後找到 **Course** **Introduction Video** field。
如果您還未新增影片，您會看到一個空的field在 **id** 欄位上。


.. image:: Images/image129.png


4. 在 **your YouTube video's ID**  欄位，輸入您的影片編碼。當您新增編碼，影片會自動出現在 field **your YouTube video's ID** 欄位上。


.. note::

    沒有儲存的按鈕。Studio會自動儲存您的改變。


舉例來說，您的課程簡介影片出現如下。


.. image:: Images/image131.png


Add Weekly Time Requirements Information
========================================


1. 在 navigation bar上，點擊 **Course Settings** ，之後點擊 **Schedule & Details** 。


2. 往下捲動到 **Requirments** section.


3. 在 **Hours of Effort per Week** 欄位，以小時為單位輸入您期望學生每週在這堂課用功的時間。
