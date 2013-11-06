
****************
創建一個 HTML 元件
****************

    .. image:: Images/image067.png

HTML 元件是最基本的元件類型。這些元件用於建造以文字為主的課程。它們可用於諸如文字、清單、聯結、圖片等資訊到單元中。 
例如，您可以在問題元件中使用這些元件來增加解釋文字，您也可使用 HTML 元件來匯入 LaTeX code到你的課程。

HTML 元件編輯器有兩種顯示模式: **Visual view** 以及 **HTML 檢視**
「Visual 檢視」提供“所見即所得” (WYSIWYG) 編輯器用以編輯已預先格式化版本的文字。「HTML 檢視」讓你可以直接編輯 HTML 原始碼。

.. note::

  當 HTML 原始碼被儲存時，Studio 將在渲染前先行處理結果。 
  在「Visual 檢視」及「HTML 檢視」之間切換以確您創建的元件看起來與您預期的一樣。

.. raw:: latex
  
      \newpage %

創建一個基本 HTML 元件
********************

**創建一個基本、空白的HTML元件**

1. 在新增新元件下，點擊 **HTML** 接著點擊 **空白** ，會出現下方的空白元件。

.. image:: Images/image069.png

2. 在空白元件中，點擊 **編輯** 開啟 HTML 編輯器。

.. image:: Images/image071.png

3. 輸入您要的資訊，接著點擊 **儲存** 。

.. note::

  若您想要加入到其它頁面或圖片的連結或或是要直接編輯 HTML，請切換到 HTML 分頁。

.. raw:: latex
  
      \newpage %

**創建一個包含樣式的基本 HTML 元件**

1. 在 **新增元件** 下方點擊 **HTML** 接著點擊 **公告** ，出現下列畫面。

.. image:: Images/image073.png

2. 點擊 **編輯** 。

  在「Visual 檢視」裡開啟文字編輯器。 用您要發表的文字取代樣式裡的文字。

.. note::

  若您想要加入到其它頁面或圖片的連結或或是要直接編輯 HTML，請切換到 HTML 分頁。

.. image:: Images/image075.png

3. 點擊 **儲存** 。

.. raw:: latex
  
    \newpage %

創建連結
*******

連結到 Handout 或圖片
==========================

要連結到一個文件、圖片或您上傳到 **檔案及上傳頁面** 的其他檔案：

1. 創建一個空白的 HTML 元件，切換到 HTML 檢視。

2. 在 HTML 對話框，創建連到您的檔案的連結。

要創建連到文件的連結，請輸入以下句法，URL OF FILE 是您上傳檔案到 **檔案及上傳** 頁面的步驟5記下的 URL，LINK TEXT 是使用者所看到可以按下的文字連結要顯示的文字。 ::

	<p><a href="[URL OF FILE]">[LINK TEXT]</a></p>

例如，要創建連結連到 “About” 頁面的 HTML 樣式的文件，其 URL 是
/c4x/edX/edX101/asset/AboutPage_Template.txt, 
則請輸入以下的原始碼： ::

  <p><a href="/c4x/edX/edX101/asset/AboutPage_Template.txt">HTML Template for
  <the "About" page</a></p>

要創建連到您已上傳的圖片的連結，請輸入以下句法，URL OF FILE 是您上傳檔案到 **檔案及上傳** 頁面的步驟5記下的 URL，LINK TEXT 是使用者所看到可以按下的文字連結要顯示的文字。 ::

  <p><img src="[URL OF FILE]"/></p>

例如，當您要建立一個連結連到 CourseImage.jpg，您記下的 URL 為
/c4x/edX/edX101/asset/CourseImage.jpg
則請輸入以下的原始碼： ::

	<p><img src="/c4x/edX/edX101/asset/CourseImage.jpg"></p>

當您使用此code，將會出現下方圖片中範例。

.. image:: Images/image078.png
  :width: 800

3. 點擊 **儲存** ，您的檔案或圖片將出現在元件中。


.. raw:: latex
  
  \newpage %
  

連結到課程單元
============

要引導學生到您課程中的特定位置，您必須要增加一個HTML連結到特定單元，請參考下列步驟：

1. 確定您課程的相對目錄。

a. 在課程設定分頁，點擊在基本資訊下方的藍色您的課程 URL 連結。

.. image:: Images/image079.png
  :width: 800

您課程的註冊頁會打開。

b. 從頁面上方瀏覽器的網址列複製 URL

c. 複製在主要網址之後，“about”之前的 URL (包含最後面的 "/")，如下所舉例： ::

	/courses/[organization]/[course_number]/[course_name]/

以 edX101: How to Create an edX Course from edX, 其完整的 URL 如下。 ::

	https://edge.edx.org/courses/edX/edX101/How_to_create_an_edX_course/about

其相對目錄如下。 ::

	/courses/edX/edX101/How_to_create_an_edX_course/

2. 確定目標單元的位置 ID。 當您創建單元時，Studio 會為每個單元產生位置 ID。 
位置 ID 使用以下的句法。::

	 i4x://<organization>/<course_number>/vertical/<url_name_of_unit>

.. note::

  要找到位置 ID，在 Studio 中開啟欲連結單元頁面，接著注意瀏覽器中的網址列中的 URL。 
  位置 ID 為結束編輯後的URL，請見以下範例。

.. image:: Images/image081.png  


3. 打開您要連結的單元。

4. 在新增元件下方，點擊 HTML，接著點擊空白。畫面上將出現一個新的空白元件。

.. image:: Images/image083.png
  :width: 800

5. 點擊 **編輯** 。

6. 在開啟的 HTML 編輯器中，點擊 HTML 分頁.

7. 接著到 number 1 輸入下列。 用您於前述步驟中取得資訊取代課程相對目錄位置，location of unit id以及連結文字。::

  <a href = "[[relative course directory]]/jump_to/[[location id of <unit]]">[link text]</a>

例如， 一個連結到 edx101 的 “Creating an HTML Component” 的單元類似於以下 ::

  <a href = "courses/edX/edX101/How_to_Create_an_edX_Course/jump_to/i4x://edX/ed
  <X101/vertical/8713e94afd074e40991dcb675d1030b5">Creating an HTML
  <Component</a>
 

.. raw:: latex
  
  \newpage %

從 LaTeX 匯入
************

您可以由匯入 LaTeX 原始碼來創建一個 HTML 元件。

.. note::

  此功能還在開發當中。

1. 在 **新增單元** 下方，點擊 **HTML** ，接著點擊 **E-text Written in LaTeX.** 

.. image:: Images/image067.png
  :width: 800

2. 在出現的元件中點擊編輯。

.. image:: Images/image083.png
  :width: 800

3. 元件編輯器會開啟。在編輯器的左上角，點擊黃色的 **Edit High Level Source** 文字。

.. image:: Images/image085.png
  :width: 800

4. 在開啟的 **High Level Source Editing** 畫面中，以您的 LaTeX 原始碼取代範例程式碼。

.. image:: Images/image087.png
  :width: 800

5. 點擊 **Save and compile to edX XML** 以轉換 LaTeX 原始碼到 edX XML 程式碼。

.. note::

  Studio 使用第三方 LaTeX 處理器來轉換 LaTeX 程式碼到 XML，LaTeX 處理器必須是在啟動中的狀態才能使用。

6. 點擊 **儲存** ，檢查您新建的元件是否看起來跟您預想的一樣。

