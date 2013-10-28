
**************************
在Studio中創建一門課程
**************************

一旦您已經創建一個課程，而您準備去創建那個課程的內容。

.. warning::

	這個Studio的alpha版本沒有版本控制或自動更新您的瀏覽器between refreshes. 
	Versioning is planned for future refresheseleases, 但是，in the meantime, only one author should edit a unit, in one
	browser, on only one tab.  如果一個unit使用多個瀏覽器進行編輯，這個session將不會顯示任何警告就會將最後儲存內容覆蓋掉過去所儲存的內容。
	並且，舊的瀏覽器sessions可以覆蓋更多最新的內容，所以, 在每次開始一個private unit或編輯一個public unit的草稿這些工作之前請刷新您的瀏覽器。


簡介
************

正如一個offline課程，在一個線上課程內容被細分成更小的碎片。
在Studio中，這些碎片被分類叫**sections，subsections以及units** 
Units，in turn，被做成 **components** 包含了您課程內容的實際內容。

Sections，舉例來說，可對應您的課程的第幾週，而subsections常常是對應您的lessons、
回家作業或者考試。
一個lesson可以選擇各units的種類，像是影片、文字、圖片、討論以及問題所交織而成。
這是一個具有互動代表性的教材，您會cover in a typical class period.

在**Course Outline** 頁，您可以看到全部的sections、subsections以及units在您的課程中一目了然，
還有subsections是否為公開或私人。


    .. image:: Images/image029.png
       :width: 800

    .. image:: Images/image031.png
       :width: 800

.. raw:: latex
  
	\newpage %

節
*******

一個section是最頂層的類可以用它來組織您的課程。
許多教師根據課程在第幾週來命名
-像是，section 1被命名為第一週、section 1被命名為第二週，以此類推。
Sections包含subsections，which in turn contain units.

您可以設置一個individual 發佈日期給每一個在您課程中的section。
直到釋出日期已經通過之前，在section中沒有內容會被看見。

要了解更多有關如何創建一個section的資訊，請看
:doc:`create_section_sub_section`.

.. raw:: latex
  
	\newpage %

小節
**********

一個subsection是一個section的一個subcategory。許多教師根據他們課程的主題去命名他們的subsections。
Subsection命名顯示along with section的命名在左側的pane當您在Edge上觀看您的課程。

    .. image:: Images/image033.png

您可以設定subsections當作您創造作業種類當您設定grading。
您可以include作業在subsection的body中。

您可以對您的課程中的每個subsection設定一個單獨的發佈日期。
直到它的發佈日期已經通過之前，在subsection中沒有內容會被看見。
如果您沒有設定一個發佈日期，這個subsection已經有和它的section相同的發佈日期。


要了解更多有關如何創建一個subsection，請看
:doc:`create_section_sub_section`.

.. raw:: latex
  
	\newpage %

單元
****

一個單元是一個幫助您組資您的課程教材之進一步的類別。
單元中包含建立lessons區塊之Component。
單元不會顯示在左側的pane with section and subsection headings。
取而代之的是，當您在Edge上觀看您的課程，每個單元顯示成 course accordion在頁面上方的一部分，
接下來的頁面顯示出一個subsection有兩個Units。

    .. image:: Images/image035.png

請注意，默認情況下，所有的單元被設定成 **Private.** 為了顯示一個單元給學生，
您必須明確的改變unit的可見度為 **Public.**
要了解更多資訊請看 :doc:`set_content_releasedates` .

.. raw:: latex
  
	\newpage %


元件 
*********
一個component為一個單元的部分包含您實際的課程內容。
當您在頁面上方的course accordion中hover over這個單元，所有在unit中components的名稱會顯示。

.. image:: Images/image037.png    
 :width: 800
這裡有四種components：討論components、HTML components、問題components，以及影片components。
了解更多資訊，請看:doc:`create_discussion`, :doc:`create_html_component`, :doc:`create_problem`, and :doc:`create_video` . 




