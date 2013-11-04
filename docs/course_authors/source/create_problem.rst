
*******
創建問題
*******

概要
****


「問題」單元允許您在您的課程中新增互動式及自動評分的練習，您可以在Studio創建許多不同種類的問題。
預設的情況下，所有的問題都是不評分練習問題。要將這些問題改成評分問題，請改變小節中的作業種類。

創建一個問題時，需要決定：

• 您想要創建的問題種類。

• 這個問題所佔的權重。

• 您是否想要隨機排列這問題。

• 要如何結束一個問題，譬如需要多少學生參與回答 (當然是在截止時間結束前)。

• 您想要如何提供回饋給學生們；是否顯示答案。

這個課程包含許多地方有更多資訊有關創建練習以及整合它們到您的課程中。

• `Writing Exercises <https://edge.edx.org/courses/edX/edX101/How_to_Create_an_edX_Course/courseware/a45de3baa8a9468cbfb1a301fdcd7e86/d15cfeaff0af4dd7be4765cd0988d172/1>`_ has more in-depth discussion about problem types, and some general pedagogical considerations for adapting to the online format and a `Gallery of Response Types <https://edge.edx.org/accounts/login?next=/courses/edX/edX101/How_to_Create_an_edX_Course/courseware/a45de3baa8a9468cbfb1a301fdcd7e86/3ba055e760d04f389150a75edfecb844/1>`_

•  `Appendix E <appendices/e.html>`  包含了許多不同問題回應種類之XML的文件。

•  The `Discussion Forum <https://edge.edx.org/courses/edX/edX101/How_to_Create_an_edX_Course/discussion/forum">`_  for this class is a good place to ask questions about exercise types, report any errors or oddities that you may encounter, and get technical support.

•  Creating problems for the online format opens a new playing field in the educational process. A big part of the community aspect of edX is to initiate and grow a `Creative Problems <https://edge.edx.org/courses/edX/edX101/How_to_Create_an_edX_Course/wiki/edx101/creative-problems/>`_ . Please look here to be inspired by new approaches when first making your class. Please also come back to post interesting approaches that you came up with while running your class, and to share with the community what worked well and what did not.

**Simple Editor and Advanced Editor**


Studio提供兩個介面來編輯問題components。
 
• **Simple Editor** 允許您直觀的去編輯問題，不需要用XML。

• **Advanced Editor** 轉換這些問題成edX's XML標準並且允許您直接去修改那個XML。想了解更多有關XML不同問題種類，請看 `Appendix E <appendices/e.html>` .


一些簡單的問題範例，包括多個選擇，在Simple Editor中開啟並且允許您在Advanced Editor選擇。更多複雜的問題種類，像是Circuit Response，在Advanced Editor中開啟。

.. note::
	您可以隨時點擊在Simple Editor介面中的"Advanced Editor"就可以從Simple Editor切換到Advanced Editor。但是，如果新增一個component就沒有辦法從Advanced Editor切換回Simple Editor。

開啟Advanced Editor，請點擊Simple Editor右邊角落的  **Advanced Editor**  。

.. image:: Images/image275.png
    :width: 600px
   

接著是一個在Advanced Editor中的多選題。

.. image:: Images/image276.png
    :width: 600px

.. raw:: latex
  
  \newpage %


問題種類
************

連結到不同問題種類的敘述-brief。並且匯入連結給所有XML，etc。

您可能想要創建一個超過一個回應類型的問題。舉例來說，您可能想要創建一個多選題，並且要求學生去解釋他或她的回應。
您可能也想要學生能夠檢查這些同時有多個問題的答案。為了實現這個工作，您可以匯入一個多選題到一個有單一的問題component。 (LINK)

.. raw:: latex
  
  \newpage %

隨機化
***********


**rerandomize** 設定可以決定是不是要任何問題隨機的輸入，是不是在任何時間一個學生看到這個問題時會不會隨機化。
(這個只可以應用在可以隨機產生數值變數的問題。)

.. raw:: latex
  
  \newpage %

分數及加權
******************

每個問題都儲存了一個 **point score** 給提交的回應。而一個學生取得的分數是由學生提交回應的正確數量除以問題的maximum score。
預設的maximum score或者權重，是這問題擁有回應輸入種類的整數值。
因此，這個問題的權重屬性帶有一個回應輸入種類被設定為1 (一分)。您可以藉由手動改變問題的 **weight** 屬性值成另一個數字來改變最小分數給這個individual問題，
當您做完這件事，分數的數值明確顯示在問題的標題旁邊 ( 一個小數的精準度)。

**WEIGHT: 0 POINTS**


這些分數被儲存在問題中，but they only contribute to a student's grade in the course if they are part of a subsection marked as graded. 
想要了解更多資訊，請看material on attempts and closing problems in 7B: Feedback and Grading.

.. raw:: latex
  
  \newpage %

**Computing Point Scores**

The point score of a response for a problem reflects the correctness of the response and is recorded as the number of points earned out of the maximum
possible score for the problem (also known as the problem weight). The formula used for computing the recorded point score is the following:

•  **point score of response = problem weight * (# inputs correct / # total inputs)**

•  **point score of response** is the point score "earned" by this response for the problem.
   
•  **problem weight** is the maximum possible point score that can be earned for the problem. By default, this is the integer number of response types in that problem. This can be changed to another value by setting the weight attribute of the problem, as described in Setting Problem Attributes.
  
• **# inputs correct** is the number of values for this response that were evaluated as correct by the response type fields.
   
• **# total inputs** is the total number of response type fields in the problem.

.. raw:: latex
  
  \newpage %
   
**Examples**

接下來是一些設定問題權重和計算分數的例子。


**Example 1**

一個問題有兩種回應輸入以及一個空的權重屬性有一個最小分數2.0分。

一位學生回應這個由一個正確輸入值和一個不正確輸入值的問題將被標記為擁有1.0分到2.0分的可能性。


**Example 2**

一個問題有三種回應輸入種類以及一個權重屬性為12有一個最小分數12.0分。

一位學生回應這個由一個正確輸入值和兩個不正確輸入值的問題將會被標記為擁有4.0分到12.0分的可能性。


**Example 3**

一個問題有四種回應輸入種類以及一個權重屬性為2有一個最小分數2.0分。

一位學生回應這個由兩個正確輸入值和兩個不正確輸入值的問題將會被標記為擁有0.5到1.0分的可能性。

**PROBLEM: 20.0 POINTS**

• 這個問題的權重屬性已經從預設值被改變。

• 整個問題有多少分？

• 這個問題中的權重值設定為多少？

• 這個問題中有多少回應輸入？

• 這個問題的預設最小分數是多少？

• 這個問題中如果對一個而其餘錯，那分數怎麼算？

.. raw:: latex
  
  \newpage %

關閉
*****
為了停止接受回應並且紀錄分數，問題可以被 **closed.** 關閉問題不會顯示一個 **Check** 按鈕。
學生在一個關閉的問題中依然可以看到問題、答案，以及顯示說明，但是他們再也不能檢查他們的工作、提交回應，或者改變他們儲存的分數。


您可以用許多方式關閉問題：


• 設定一個截止日期給這些在subsection中的問題。注意您不可以設定截止日期給individual問題 -- 只能是包含subsections (作業)。 預設的情況下，截止日期不會被設定。要設定一個截止日期，請看 LINK。

• 指定一個寬限期給您的課程。注意這個寬限期顯示給全部的課程。要設定一個寬限期，請看 LINK。
設定
• Set the number of attempts for the individual problem component. The attempts setting determines the number of times a student is allowed to check their answer by clicking Check before the problem closes. If this field is left blank, a student has unlimited attempts. If you specify a number for the attempts setting, the number of total allowed and remaining attempts appears next to the Check button for the problem. Problems with a limited number of attempts also always display a Save button that allows response values to be saved without being submitted. When there is only one submission left, the student will receive a warning, and the Check button will be replaced with a Final Check button. When no attempts are left, both the Save and Check button will disappear.For more information, see Problem Attributes.

• Manually increase the number of attempts left for a given problem for a particular student from the Instructor tab in the live view of your course, when accessed in the Instructor view on Edge. This is recommended only for unusual situations, such as if you have to fix live problems during an exam.

.. raw:: latex
  
  \newpage %

Feedback
********

Stuido包含許多可以提供feedback給學生的工具： **Check** 按鈕， **Show Answer** 按鈕，以及 **Attempts** 設定。當您使用 **Show Answer** 按鈕，您也可以提供一個答案的詳細說明。

TBD-SCREENSHOT OF PROBLEM WITH THESE ELEMENTS CIRCLED

**Check Button**

學生點擊 **Check** 按鈕去提交一個回應。這個問題module就會執行接下來的步驟。

• 同意並儲存回應到每個輸入。

• 使用一個automatic grader去檢查回應值來對應到正確答案或解答。

• 目視標記一個正確的回應是一個綠色的勾勾以及不正確的回應是一個紅色叉叉。

• 儲存學生回應這題得到的分數。

如果一位學生想要去儲存但是不要提交回應，那位學生可以點擊 **Save** 。

接下來的問題，輸入一個回應，之後點擊 **Check** 。這個問題就會告訴您，您的回應是正確還是不正確的。

此時，雖然您不會看見它，但是分數還是會自動儲存到您提交的回應。

.. image:: Images/image277.png
    :width: 600px

**Show Answer button**

當一位學生點擊 **Show Answer** ，這個問題就會在對應回應輸入的旁邊顯示出正確答案並且顯示您已經提供的額外解釋。
**Show Answer** 是由問題編輯器中的 **showanswer** 屬性所控制。
它可能被設定為絕對無法看見、總是被看見或者只有當問題被關閉後才可看見。 [Reference: Setting Problem Attributes.]

接下來的問題， **Show Answer** 按鈕在學生對答案做了至少一個attempt後出現。輸入一個回應您知道是錯的，之後點擊 **Check** 。

.. image:: Images/image278.png
    :width: 600px

現在，點擊 **Show Answer** 去查看正確答案以及它的解釋。

.. image:: Images/image279.png
    :width: 600px


.. raw:: latex
  
  \newpage %



創建問題
****************

.. note::
    
    您可以也通過您的課程匯入non-graded練習題。

為了增加互動性，使用問題component，來自動graded練習題到給您的課程內容。這個component允許您去匯入一個說明是學生點擊 **Show Answer** 時可以看見的。

 Studio提供多個templates讓您使用。另一方面，您可以在XML創建您自己的問題類型。
 要了解更多有關不同問題類型問題的訊息，請看 `Appendix E <appendices/e.html>`.  
   

1. 在 **Add New Component** 之下，點擊 **Problem** 。

.. image:: Images/image096.png
    :width: 600px

**Select Problem Component Type** 畫面顯示。預設情況下， **Common Problem Types** 標籤被選擇。

.. image:: Images/image097.png
    :width: 600px

要觀看更多複雜問題類型的列表，點擊 **Advanced** 標籤。


.. image:: Images/image099.png
    :width: 600px


2. 點擊您想要的問題類型。

.. note::
    
    為了在XML中創建您自己的問題，點擊 "Empty" 來開啟一個空的XML編輯器。

A new problem component with sample template text appears.

舉個例子，如果您點擊 **Multiple Choice** ，接下來的問題component會顯示。

.. image:: Images/image101.png
    :width: 600px



3. 點擊 **Edit** 。這會開啟Simple Editor給問題component。接下來的例子會顯示出這個視圖給一個多選問題。

.. image:: Images/image103.jpg
    :width: 600px


4. 設定問題屬性。


在 **display_name** 欄位，填入您想要學生在hovers over the icon in the bar at the top of the page時看見的文字。這個文字也會顯示為 a header for the problem。


a. 在 **weight** 欄位中，設定一個權重值給問題。如果您想要這個問題被作為一個practice問題，設定這為零 (0)。

b. 在 **rerandomize** 欄位，

c.  在 **attempts** 欄位，具體指明您想要允許學生attempts的數量。
  
d.  在 **showanswer** 欄位，輸入接下來的設定。

.. raw:: latex
  
  \newpage %

**Reference**

• **never** = 顯示答案按鈕永遠不會被看見。

• **closed** = 顯示答案按鈕不論是在截止日期已經過了，或者學生已經沒有attempts left，都不會被看見。

• **attempted** = 顯示答案按鈕在學生已經檢查過答案一次之後出現，不論是否正確。

• **always** = 顯示答案按鈕永遠出現。


5. 修改問題的文字，之後點擊 **Save** 來儲存並且檢查您的工作。確認發布您現在正在工作的草稿來即時觀看問題。

.. raw:: latex
  
  \newpage %

修改釋出的問題
*************************

   **WARNING: 當您已經釋出問題之後要做修改請務必格外小心!**

Currently, problems cache the following information per student:

• 這位學生的最後 **submitted** 回應. 
  
• 學生最後回應所獲得的分數。

• 問題的最小值分數。

當學生提一個回應給問題時這個訊息會被上傳。如果學生重新整理這個 **Progress** 頁面，解答不是被重新檢查。If a student refreshes the page of a problem, the latest version of the problem statement is loaded, but their previous response is NOT reevaluated. Rather, the previous response is loaded on top of the current problem statement. That is **existing** student responses for a problem are not reevaluated if the problem statement or attributes are changed, until a student goes back and resubmits the problem. Furthermore, as of the time of writing, if the problem weight attribute is changed, stored scores are re-weighted (without rechecking the response) when the student reloads the **Progress** page.

舉例來說，您可能會釋出一個有兩個輸入的問題。當一些學生已經提交了答案之後，如果您改變這個答案中輸入的其中一個，則目前學生的分數不會更新。

Example: 如果您改變輸入的數量變成三個，學生在這個改變之前提交答案則會有一個分數為 0, 1, 或 2到2.2。學生提交答案在這個改變之後，則同樣的問題會有分數 0, 1, 2, 或 3到3.0 。

然而，如果您進入並且改變這個問題的權重，目前的分數當您重新整理 **Progress** 時會更新。

Note that the behavior of re-grading in case of error is an edX Edge case. It is dependent on the implementation of grading, and may change. The goal in the future is to include re-grading that will allow some basic updates to live problems, whether or not students have submitted a response.

.. raw:: latex
  
  \newpage %


Workarounds
===========

如果您已經以某種方式修改了一個釋出的問題而影響到評分，您有兩個選項。注意這兩個選項需要您去要求您的學生回去並重新提交問題。


1.  增加相同問題component中的attempts在問題上的數量。之後要求所有在您這堂課的學生重做這個問題。

2.  刪除整個在Studio中的問題component並且創建一個新的問題component，其內容和設定是您想要的。之後要求所有在您這堂課的學生回到這個作業並且完成問題。

檢查您在Edge上的 **Progress** 視圖或 **Instructor** 標籤作為在觀看分數的unit中的描述以查看是否分數被儲存如您所料。如果那裡有儲存分數的問題讓您不能理解或者不能修正，連繫在Studio幫助頁面支援。

For a discussion of some trade-offs and some suggestions for cleaner solutions in the future, see the following `discussion thread <http://help.edge.edx.org/discussions/questions/73-what-if-you-discover-that-a-live-problem-is-wrong">`_ 在Studio上的help desk。

您可以匯入多個單一問題component中不同種類的問題，甚至當您創建一個問題時，您可以選擇一個particular template。一個template僅僅是一個由XML編輯已經填寫好的文字。您可以新增或者取代這個template的文字。
