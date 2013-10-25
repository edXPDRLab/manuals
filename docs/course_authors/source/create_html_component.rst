
************************
創建一個HTML組件
************************

    .. image:: Images/image067.png

HTML組件是最基本的組件類型。 這些組件用於建造以文字為主的課程。
它們用於增加資訊諸如文字、清單、聯結、圖片到units。 例如，你可以在問題組件中使用這些組件來增加解釋文字。
你也可使用HTML組件來匯入LaTeX code到你的課程。

HTML組件編輯器有兩種顯示: **Visual view**以及**HTML view.**
Visual view 提供“what you see is what you get” (WYSIWYG) 編輯器用以
編輯已預先格式化版本的文字。HTML view讓你可以直接編輯HTML code。

.. note::

  當HTML code被儲存時，Studio再渲染前先處理。 
  在Visual view及HTML view之間切換以確保你創建的組件看起來與你預期的一樣。

.. raw:: latex
  
      \newpage %

創建一個基本HTML組件
*****************************

**創建一個基本、空白的HTML組件:**

1. 在新增新組件下，點擊**html**接著點擊**Empty.**
會出現下方的空白組件。

.. image:: Images/image069.png

2. 在空白組件中，點擊**Edit.** 開啟HTML編輯器。

.. image:: Images/image071.png

3. 輸入你要的資訊，接著點擊**Save.**

.. note::

  若你想要加入到其它頁面或圖片的連結或或是要直接編輯HTML，切換到HTML分頁。

.. raw:: latex
  
      \newpage %

**創建一個包含樣式的基本HTML組件，你可以使用:**

1. 在**Add New Component,**下方點擊**html**接著點擊**Announcement.** 
出現下列畫面。

.. image:: Images/image073.png

2. 點擊**Edit.**

  在Visual view裡開啟文字編輯器。 用你要發表的文字取代樣式裡的文字。

.. note::

  若你想要加入到其它頁面或圖片的連結或或是要直接編輯HTML，切換到HTML分頁。

.. image:: Images/image075.png

3. 點擊**Save.**

.. raw:: latex
  
    \newpage %

創建連結
************

連結到Handout或圖片
==========================

要連結到一個文件、圖片或你上傳到Files & Uploads頁面的其他檔案:

1. 創建一個空白的HTML組件，切換到HTML view.

2. 在HTML框, 創建連到你的檔案的連結。

要創建連到文件的連結，輸入以下句法，URL OF FILE是你上傳檔案到Files & Uploads頁面的步驟5記下的URL
LINK TEXT是使用這會按下的文字。 ::

	<p><a href="[URL OF FILE]">[LINK TEXT]</a></p>

例如，要創建連結連到“About”頁面的HTML樣式的文件，其URL是
/c4x/edX/edX101/asset/AboutPage_Template.txt, 
使用以下code。 ::

  <p><a href="/c4x/edX/edX101/asset/AboutPage_Template.txt">HTML Template for
  <the "About" page</a></p>

要創建連到你以上傳的圖片的連結，輸入以下句法，
URL OF FILE是你上傳檔案到Files & Uploads頁面的步驟5記下的URL
LINK TEXT是使用這會按下的文字。 ::

  <p><img src="[URL OF FILE]"/></p>

例如, to create a link to the CourseImage.jpg file whose URL is
/c4x/edX/edX101/asset/CourseImage.jpg, use the following code. ::

	<p><img src="/c4x/edX/edX101/asset/CourseImage.jpg"></p>

當你使用此code，出現下方圖片。

.. image:: Images/image078.png
  :width: 800

3. 點擊**Save.** 你的檔案或圖片出現在組件中。


.. raw:: latex
  
  \newpage %
  

連結到課程Units
====================

要引導學生到你課程中的特定位置，你必須要增加一個HTML連結到特定unit. 請做到下列:

1. 確定你課程的relative directory。

a. 在課程設定分頁，點擊在Basic Information下方的藍色your course URL 連結。

.. image:: Images/image079.png
  :width: 800

你課程的註冊頁會打開。

b. 在頁面上方的address bar， locate the URL.

c. 複製在“.org”，“about”之前的URL包含forward slashes。 句法會如下。 ::

	/courses/[organization]/[course_number]/[course_name]/

例如， 以edX101: How to Create an edX Course from edX, 完整的URL
如下。 ::

	https://edge.edx.org/courses/edX/edX101/How_to_create_an_edX_course/about

其relative directory如下。 ::

	/courses/edX/edX101/How_to_create_an_edX_course/

2. 確定目標unit的location ID。 當你創建unit，Studio會為每個unit產生location ID。 
location ID使用以下的句法。::

	 i4x://<organization>/<course_number>/vertical/<url_name_of_unit>

.. note::

  要找到location ID，在Studio中開啟欲連結unit頁面接著看著遊覽器中的網址列中的URL。 
  location ID 為結束編輯後的URL，以下範例。

.. image:: Images/image081.png  


3. 要打開你要鏈接的uint。

4. 在Add New Component下方，點擊html，接著點擊Empty。
出現一個新的、空白的組件。

.. image:: Images/image083.png
  :width: 800

5. 點擊**edit**.

6. 在開啟的HTML編輯器中，點擊HTML分頁.

7. 接著到number 1輸入下列。 用你的資訊取代 relative course directory，
location of unit id以及link text。::

  <a href = "[[relative course directory]]/jump_to/[[location id of
  <unit]]">[link text]</a>

例如， 一個連結到edx101的“Creating an HTML Component”的unit
類似於以下 ::

  <a href = "courses/edX/edX101/How_to_Create_an_edX_Course/jump_to/i4x://edX/ed
  <X101/vertical/8713e94afd074e40991dcb675d1030b5">Creating an HTML
  <Component</a>
 

.. raw:: latex
  
  \newpage %

從LaTeX匯入
*****************

你可以由匯入LaTeX code來創建一個HTML組件。

.. note::

  此功能還在開發當中。

1. 在**Add New Component**下方，點擊**html**，接著點擊**E-text Written in LaTeX.**

.. image:: Images/image067.png
  :width: 800

2. 再出現的組件中點擊Edit。

.. image:: Images/image083.png
  :width: 800

3. 組件編輯器會開啟。 在編輯器的左上角，點擊
黃色的**Edit High Level Source**文字。

.. image:: Images/image085.png
  :width: 800

4. 在開啟的**High Level Source Editing**畫面中，以你的LaTeX code取代範例code。

.. image:: Images/image087.png
  :width: 800

5. 點擊**Save and compile to edX XML**以轉換LaTeX code到 edX XML
code.

.. note::

  Studio使用第三方LaTeX processor來轉換LaTeX code到XML.
  LaTeX processor必須是在作用中。

6. 點擊**Save**. 驗證你新建的組件看起來跟你預想的一樣。


