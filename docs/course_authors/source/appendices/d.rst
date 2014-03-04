.. raw:: latex
  
      \newpage %
      

======================
附錄 D: 時區
======================

    **概要**
    一次釋出課程教材讓所有學生可以看見，在具體指名的設定時間，有截止日期的作業將一次be due給所有學。
	然而，許多地方在edX及Studio提出一種時間設定無須指定時區。除非另有規定，大部分日期和時間在Studio和edX中是UTC而不是您當地的時區!
	當您指定日期和時間設定沒有一個時區標籤，您需要轉換值為UTC。
	您也應該確保學生和老師知道如何理解您課程中的時間設定。
	
    **詳述**
    時間被儲存在一個特別的時區中。然而，這個時區可能不會顯示在介面中。未標籤的時間值以UTC格式被指定、儲存，和觀看。

	
    Edx和Studio處理時區如下。

    •	所有時間，標籤和未標籤，都被儲存在伺服器上以UTC格式 (a.k.a. UTC or Z)。
    •	未標籤時間被顯示在不論是Studio或edX/Edge上以UTC格式。
    •	在Studio中一個特別時區的時間標籤被具體指明在那個時區，並且轉換為UTC。 (這是罕見的。)

    在Studio中的設定，被標籤為一個時區，像是課程開始和結束時間，輸入設定在時區中具體指明出來 (通常是您當地時區)。
	
    未標籤時區的時間設定，像是課程內容的釋出日期和截止日期，從您的當地時區轉換，以及設定日期和時間以UTC格式。您可以使用線上時區轉換來轉換成為您的當地時區時間。
	
    *請注意當您使用一個線上轉換，進入日光節約日子時間時同時考慮到一天的時間。*

																																		
    例如美國東部標準時間是 "UTC-5"，所以在Studio中紐約的冬天下午5:00（17:00）截止日期應輸入為晚上10:00（或22:00）。 美國日光節約時間，然而，是UTC-4，所以在Studio中紐約的夏天截止日期下午5:00應該輸入為下午9:00。

    
	在edX/Edge以學生的角度這些時間設定大部分也不會被標籤。 當您設定了一個作業的截止日期，請確定告訴學生該如何解釋這個截止日期。您可以選擇下列選項之一。

    •	隨時提前通知學生，除非另有標籤，都會被顯示成UTC格式，指點他們到一個時區轉換來轉換他們當地時區時間。
    •	Allow students to assume that all due dates are specified in their local time zone, and specify an unadvertised grace period to invisibly extend all the due dates in your course. For example, some courses set a grace period of "1 day, 6 hours, and 1 minute" to accommodate differences in time zones and any potential system issues.

    *請注意一般不建議設定一個寬限期。它可能導致問題沒有關閉 "when they should"，以及可能會誤導您的學生。*

    如果您有進一步關於指定時間和時區的問題，或者正遭受截止日期或釋出日期不一致的特性，請從edX Studio的幫助頁面聯絡我們。

    **參考文獻**

    http://help.edge.edx.org/discussions/questions/61-time-zones

    http://help.edge.edx.org/discussions/questions/23-grace-periods
