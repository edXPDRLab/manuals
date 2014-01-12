.. _Exporting and Importing a Course:

#####################################
匯出或匯入課程
#####################################

You can :ref:`Export a Course` and :ref:`Import a Course` through Studio.

.. _Export a Course:

*************** 
匯出一門課程
***************
There are several reasons you may want to export your course:

* To edit the XML in your course directly
* To create a backup copy of your course, which you can import if you want to revert the course back to a previous state
* To create a copy of your course that you can later import into another course instance and customize
* To share with another instructor for another class
 
 
當您匯出您的課程時，Studio 會創建一個 **.tar.gz** 檔案，其中包含以下課程資料：
 
* Course content (all Sections, Subsections, and Units)
* Course structure
* Individual problems
* Static pages
* Course assets
* Course settings
 

匯出的檔案不會包含以下資料：
 
* User data
* Course team data
* Forum/discussion data
* Certificates

To export a course:
 
#. From the **Tools** menu, select **Export**.
#. Click **Export Course Content**.

When the export completes you can then access the .tar.gz file on your computer.


.. _Import a Course:

*************** 
匯入課程
***************

.. warning::

	Content of the imported course replaces all the content of this course. 
	**You cannot undo a course import**. We recommend that you first export the current course, 
	so you have a backup copy of it.
 
There are several reasons you may want to import a course:

* To run a new version of an existing course
* To replace an existing course 
* To load a course you developed outside of Studio


The course that you import must be in a .tar.gz file (that is, a .tar file compressed with GNU Zip). 
This .tar.gz file must contain a course.xml file in a course data directory. The tar.gz file must
have the same name as the course data directory. It may also contain other files.
 
若您的課程使用傳統舊的格式包裝，您可能無法在 Studio 中編輯您的課程資料，即使其可能正確地在 Edge 裡顯示。
要確定您的課程是完全可編輯的，必須確定您所有的教材都被嵌入至一個「單元」中。
 
The import process has five stages. During the first two stages, you must stay on the Course Import page. 
You can leave this page after the Unpacking stage has completed. We recommend, however, 
that you don't make important changes to your course until the import operation has completed. 
 
To import a course:
 
#. From the **Tools** menu, select **Import**.
#. Click **Choose a File to Import**.
#. Locate the file that you want, and then click **Open**.
#. Click **Replace my course with the one above**.

