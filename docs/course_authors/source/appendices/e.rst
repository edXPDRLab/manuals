.. raw:: latex
  
      \newpage %


================
附錄 E: 問題類別
================

選項響應
========

選項響應允許學生從一群選項組合中，從下拉式選單中選出正確的答案。

選項響應類似選擇題，有些概念上不同之處如下所列：

* 選擇題使用的單選按鈕比較適合學生在較長的敘述中選出答案。

* 選項響應使用的下拉式選單的格式，適合學生先思考一個可能的答案再從選單中尋找，而非純粹認出這個答案。

* 選擇題的格式較為明確清晰，所以更為適合用在較為複雜的問題以及答案的組合應用上，讓學生能夠適度地暫停思考可能的答案。

範例問題如下：

.. image:: ../Images/image287.png
    :width: 600  

**問題代碼**

.. code-block:: xml

  <problem>

   <p>Option Response is most similar to __________.</p>

    <optionresponse>
     <optioninput
       options="('Multiple Choice','String Response',
                'Numerical Response','External Response',
                'Image Response')"
      correct="Multiple Choice"/>1
    </optionresponse>

   <solution>
     <div class="detailed-solution">
       <p>Explanation</p>
        <p>Like Option Response, Multiple Choice also allows students to select
       from a variety of pre-written responses.</p>
     </div>
    </solution>
  </problem>



**樣板**

.. code-block:: xml

  <problem>

    <optionresponse>
     options="('A','B')"
      correct="A"/>
    </optionresponse>

    <solution>
      <div class="detailed-solution">
      </div>
    </solution>
  </problem> 



**XML 屬性資訊**

<optionresponse>


  .. image:: ../Images/option_response1.png


<optioninput>

  .. image:: ../Images/optionresponse2.png


.. raw:: latex
  
      \newpage %


選擇題 
======

選擇題允許學生從一群選項組合中，以單選按鈕清單的形式選出正確的答案。

一個選擇題可以擁有超過一個以上的答案，端看您在 XML 中怎樣描述並標記哪些選項是正確的。如果所有的選項都是錯的，那麼這是一個錯誤格式的選擇題。

選擇題類似於選項響應，有些概念上不同之處如下所列：

* 選擇題的單選按鈕讓學生容易從長敘述的選項中選出答案。

* 選項響應使用的下拉式選單的格式，適合學生先思考一個可能的答案再從選單中尋找，而非純粹認出這個答案。

* 選擇題的格式較為明確清晰，所以更為適合用在較為複雜的問題以及答案的組合應用上，讓學生能夠適度地暫停思考可能的答案。

範例問題如下：

.. image:: ../Images/image289.png
 :width: 600  

**問題代碼** 

.. code-block:: xml

  <problem>
  <p><b>Example Problem</b></p>
  <p>How many correct responses can a Multiple Choice question have?</p>
      <multiplechoiceresponse>
     <choicegroup type="MultipleChoice">
        <choice correct="false" name="one">Only one</choice>
        <choice correct="false" name="zeroone">Only zero or one</choice>
        <choice correct="true" name="zeromore">Zero or more</choice>
        <choice correct="false" name="onemore">Only one or more</choice>
        <choice correct="false" name="noone">Nobody knows</choice>
        <choice correct="true" name="someone">Somebody might know :)</choice>
    </choicegroup>
    </multiplechoiceresponse>
  <solution>
        <div class="detailed-solution">
          <p>Explanation</p>
            <p>It depends on how many choices are marked as correct in the underlying XML.</p>                  
  <p>Note that if all choices are marked as incorrect, there is no
          correct response.</p>
        </div>
    </solution>
  </problem>


**樣板** 

.. code-block:: xml

  <problem>

  <multiplechoiceresponse>
    <choicegroup type="MultipleChoice">
      <choice correct="false" name="a">A</choice>
      <choice correct="true" name="b">B</choice>
    </choicegroup>
  </multiplechoiceresponse>

  <solution>
    <div class="detailed-solution">

    </div>
  </solution>
  </problem>


**XML 屬性資訊**


<multiplechoiceresponse>

.. image:: ../Images/multipleresponse.png


<choicegroup>

  .. image:: ../Images/multipleresponse2.png


<choice>

  .. image:: ../Images/multipleresponse3.png


.. raw:: latex
  
      \newpage %


核取方塊
========

核取方塊允許學生從一群選項組合中，以核取方塊清單的形式選出零或多個的答案。

備註：一個問題本身若使用核取方塊來描述正確答案的組合，作答時所有被標記為 "true" 的選項都必須選擇出來才會被判定為正確。

比較特別的是，“所有選項都被選起" 可以是一種正確的答案。但與選擇題不同的地方在於，一定至少要有一個選項被選起，沒有選項被選起是種錯誤的格式。

範例問題如下：

.. image:: ../Images/image290.png
 :width: 600  


**問題代碼**

.. code-block:: xml

  <problem>
  <startouttext/>
    <p>How many correct responses can a Checkbox question have?</p>

  <choiceresponse>
  <checkboxgroup>
  <choice correct="false"><text>Zero</text></choice>
  <choice correct="true"><text>One</text></choice>
  <choice correct="false"><text>Two or more</text></choice>
  <choice correct="false"><text>Nobody knows</text></choice>
  <choice correct="true"><text>Somebody might know :)</text></choice>
  </checkboxgroup>
  </choiceresponse>
  </problem>


**樣板**

.. code-block:: xml

  <problem>

  <choiceresponse>
  <checkboxgroup>
  <choice correct="false"><text>Zero</text></choice>
  <choice correct="true"><text>One</text></choice>
  </checkboxgroup>
  </choiceresponse>
  </problem>

.. raw:: latex
  
     \newpage %


字串響應
========

字串響應提供了一個輸入方塊，學生可以輸入一行文字作為答案。

字串響應並不提供任何作答輔助，所以這也間接鼓勵學生將其想法以各種形式，完成描述出來。

需要注意的是，由於學生的答案必須一字不差地符合答案的設定才能被判定為正確，因此這可能會在一些較為多元的答案格式 (例如日期) 上造成一些困擾。

範例問題如下：

.. image:: ../Images/image291.png
 :width: 600   

**問題代碼**

.. code-block:: xml

  <problem>
    <p><b>Example Problem</b></p>
    <p>What is the name of this unit? (What response type is this?)</p>
    <stringresponse answer="String Response" type="ci">
      <textline size="20"/>
    </stringresponse>
    <solution>
      <div class="detailed-solution">
        <p>Explanation</p>
        <p>The name of this unit is "String Response," written without the punctuation.</p>
        <p>Arbitrary capitalization is accepted.</p>
      </div>
    </solution>
  </problem>

**樣板**

.. code-block:: xml

  <problem>
    <stringresponse answer="REPLACE_THIS" type="ci">
      <textline size="20"/>
    </stringresponse>
    <solution>
      <div class="detailed-solution">
      </div>
    </solution>
  </problem>

**XML 屬性資訊**

<stringresponse>

  .. image:: ../Images/stringresponse.png

<textline>

  .. image:: ../Images/stringresponse2.png


.. raw:: latex
  
      \newpage %


數值響應
========

數值響應提供了一個輸入方塊，學生可以輸入一個數字作為答案，不過數值的表示方式則必須遵守一定的規範。

答案本身只要落在容忍的範圍內，就會被判定為正確。

預期的答案可以是個明確的數值，或是一段 Python 腳本計算的結果。

允許的輸入答案形式包含了 ``<formulaequationinput />`` and ``<textline />`` 兩種。
不過用 ``<textline math="1" />`` 格式描述的數學問題，可能會因為使用不同的分析器處理而有不同的結果，這會造成學生作答時的困難。
因此我們強烈建議只使用 ``<formulaequationinput />`` 這種格式，請見下面的範例問題。

範例問題如下：

.. image:: ../Images/image292.png
 :width: 600   


**問題代碼：**:

.. code-block:: xml

  <problem>
    <p><b>Example Problem</b></p>

  <p>What base is the decimal numeral system in?
      <numericalresponse answer="10">
          <formulaequationinput />
      </numericalresponse>
  </p>

    <p>What is the value of the standard gravity constant <i>g</i>, measured in m/s<sup>2</sup>? Give your answer to at least two decimal places.
    <numericalresponse answer="9.80665">
      <responseparam type="tolerance" default="0.01" />
      <formulaequationinput />
    </numericalresponse>
  </p>

  <!-- Use python script spacing. The following should not be indented! -->
  <script type="loncapa/python">
  computed_response = math.sqrt(math.fsum([math.pow(math.pi,2), math.pow(math.e,2)]))
  </script>
    
  <p>What is the distance in the plane between the points (pi, 0) and (0, e)? You can type math.
      <numericalresponse answer="$computed_response">
          <responseparam type="tolerance" default="0.0001" />
          <formulaequationinput />
      </numericalresponse>
  </p>
  <solution>
    <div class="detailed-solution">
      <p>Explanation</p>
      <p>The decimal numerical system is base ten.</p>
      <p>The standard gravity constant is defined to be precisely 9.80665 m/s<sup>2</sup>.
      This is 9.80 to two decimal places. Entering 9.8 also works.</p>
      <p>By the distance formula, the distance between two points in the plane is
         the square root of the sum of the squares of the differences of each coordinate.
        Even though an exact numerical value is checked in this case, the
        easiest way to enter this answer is to type
        <code>sqrt(pi^2+e^2)</code> into the editor. 
        Other answers like <code>sqrt((pi-0)^2+(0-e)^2)</code> also work.
      </p>
    </div>
  </solution>
  </problem>

**樣板**

精確值

.. code-block:: xml

  <problem>

    <numericalresponse answer="10">
      <formulaequationinput />
    </numericalresponse>

    <solution>
    <div class="detailed-solution">

    </div>
  </solution>
  </problem>

十進制小數答案

.. code-block:: xml

  <problem>

    <numericalresponse answer="9.80665">
      <responseparam type="tolerance" default="0.01" />
      <formulaequationinput />
    </numericalresponse>

    <solution>
    <div class="detailed-solution">

    </div>
  </solution>
  </problem>

百分比答案

.. code-block:: xml

  <problem>

    <numericalresponse answer="100">
      <responseparam type="tolerance" default="10%" />
      <formulaequationinput />
    </numericalresponse>

    <solution>
    <div class="detailed-solution">

    </div>
  </solution>
  </problem>

利用腳本計算的答案

.. code-block:: xml

  <problem>

  <!-- Use python script spacing. The following should not be indented! -->
  <script type="loncapa/python">
  computed_response = math.sqrt(math.fsum([math.pow(math.pi,2), math.pow(math.e,2)]))
  </script>

    <numericalresponse answer="$computed_response">
      <responseparam type="tolerance" default="0.0001" />
      <formulaequationinput />
    </numericalresponse>

    <solution>
    <div class="detailed-solution">

    </div>
  </solution>
  </problem>


**XML 屬性資訊**

<script>

  .. image:: ../Images/numericalresponse.png


``<numericalresponse>``

+------------+----------------------------------------------+-------------------------------+
| Attribute  |                 Description                  |              Notes            |
+============+==============================================+===============================+
| ``answer`` | A value to which student input must be       | Note that any numeric         |
|            | equivalent. Note that this expression can be | expression provided by the    |
|            | expressed in terms of a variable that is     | student will be automatically |
|            | computed in a script provided in the problem | simplified on the grader's    |
|            | by preceding the appropriate variable name   | backend.                      |
|            | with a dollar sign.                          |                               |
|            |                                              |                               |
|            | This answer will be evaluated similar to a   |                               |
|            | student's input. Thus '1/3' and 'sin(pi/5)'  |                               |
|            | are valid, as well as simpler expressions,   |                               |
|            | such as '0.3' and '42'                       |                               |
+------------+----------------------------------------------+-------------------------------+


+------------------------+--------------------------------------------+--------------------------------------+
|       Children         |                 Description                |                 Notes                |
+========================+============================================+======================================+
| ``responseparam``      | used to specify a tolerance on the accepted|                                      |
|                        | values of a number. See description below. |                                      |
+------------------------+--------------------------------------------+--------------------------------------+
|``formulaequationinput``| An input specifically for taking math      |                                      |
|                        | input from students. See below.            |                                      |
+------------------------+--------------------------------------------+--------------------------------------+
| ``textline``           | A format to take input from students, see  | Deprecated for NumericalResponse.    |
|                        | description below.                         | Use ``formulaequationinput`` instead.|
+------------------------+--------------------------------------------+--------------------------------------+


<responseparam>

  .. image:: ../Images/numericalresponse4.png

<formulaequationinput/>

========= ============================================= =====
Attribute                  Description                  Notes
========= ============================================= =====
size      (optional) defines the size (i.e. the width)
          of the input box displayed to students for
          typing their math expression.
========= ============================================= =====

<textline> (While <textline /> is supported, its use is extremely discouraged.
We urge usage of <formulaequationinput />. See the opening paragraphs of the
`Numerical Response`_ section for more information.)

  .. image:: ../Images/numericalresponse5.png


數學表達式語法
--------------

於數值響應當中，學生輸入的內容可能比普通的數字還複雜。像是 ``sqrt(3)`` 甚至 ``1+e^(sin(pi/2)+2*i)`` 都是合法而且可以計算出答案的輸入。

語法概要如下：

數字
~~~~

可接受的數字型態：

- 整數: '2520'
- 浮點數: '3.14'
- 小數: '.98'
- 科學記號: '1.2e-2' (=0.012)
- 更多的科學記號: '-4.4e+5' = '-4.4e5' (=-440,000)
- 附加 SI 後綴: '2.25k' (=2,250). The full list:

  ====== ========== ===============
  Suffix Stands for One of these is
  ====== ========== ===============
  %      percent    0.01 = 1e-2
  k      kilo       1000 = 1e3
  M      mega       1e6
  G      giga       1e9
  T      tera       1e12
  c      centi      0.01 = 1e-2
  m      milli      0.001 = 1e-3
  u      micro      1e-6
  n      nano       1e-9
  p      pico       1e-12
  ====== ========== ===============

目前支援的最大數字為正浮點數的上限值 (以 Python 語言能支援的定義)，也就是 1.7977e+308。
任何表示式中含有更大的數值是不支援的，因此最好避免這樣的情況。


預設的常數
~~~~~~~~~~

簡單而且常用的的數學及科學常數已經有定義，包含了：

- ``i`` and ``j`` as ``sqrt(-1)``
- ``e`` as Euler's number (2.718...)
- ``pi``
- ``k``: the Boltzmann constant (~1.38e-23 in Joules/Kelvin)
- ``c``: the speed of light in m/s (2.998e8)
- ``T``: the positive difference between 0K and 0°C (285.15)
- ``q``: the fundamental charge (~1.602e-19 Coloumbs)

運算元和函式
~~~~~~~~~~~~~~~~~~~~~~~

As expected, the normal operators apply (with normal order of operations): 
``+ - * / ^``. Also provided is a special "parallel resistors" operator given
by ``||``. For example, an input of ``1 || 2`` would represent the resistance
of a pair of parallel resistors (of resistance 1 and 2 ohms), evaluating to 2/3
(ohms).

At the time of writing, factorials written in the form '3!' are invalid, but
there is a workaround. Students can specify ``fact(3)`` or ``factorial(3)`` to
access the factorial function.

The default included functions are the following:

- Trig functions: sin, cos, tan, sec, csc, cot
- Their inverses: arcsin, arccos, arctan, arcsec, arccsc, arccot
- Other common functions: sqrt, log10, log2, ln, exp, abs
- Factorial: ``fact(3)`` or ``factorial(3)`` are valid. However, you must take
  care to only input integers. For example, ``fact(1.5)`` would fail.
- Hyperbolic trig functions and their inverses: sinh, cosh, tanh, sech, csch,
  coth, arcsinh, arccosh, arctanh, arcsech, arccsch, arccoth

.. raw:: latex
  
      \newpage %



方程式響應
============

The Formula Response input type accepts a line of text representing a
mathematical expression from the student and evaluates the input for equivalence
to a mathematical expression provided by the grader. Correctness is based on
numerical sampling of the symbolic expressions.

The syntax of the answers is shared with that of the Numerical Response,
including default variables and functions. The difference between the two
response types is that the Formula Response grader may specify unknown
variables. The student's response is compared against the instructor's
response, with the unknown variable(s) sampled at random values, as specified
by the problem author.

The answer is correct if both the student-provided response and the grader's
mathematical expression are equivalent to specified numerical tolerance, over a
specified range of values for each variable.

This kind of response type can handle symbolic expressions. However, it places
an extra burden on the problem author to specify the allowed variables in the
expression and the numerical ranges over which the variables must be sampled in
order to test for correctness.

A further note about the variables: when the following Greek letters are typed
out, an appropriate character is substituted:

  ``alpha beta gamma delta epsilon varepsilon zeta eta theta vartheta iota
  kappa lambda mu nu xi pi rho sigma tau upsilon phi varphi chi psi omega``

Note: ``epsilon`` is the lunate version, whereas ``varepsilon`` looks like a
backward 3.

範例問題如下：

.. image:: ../Images/image293.png
 :width: 600   

**問題代碼：**:

.. code-block:: xml

  <problem>
    <p><b>Example Problem</b></p>
    <p>This is a short introduction to the Formula Response editor.</p>

    <p>Write an expression for the product of R_1, R_2, and the inverse of R_3.</p>
    <formularesponse type="ci" samples="R_1,R_2,R_3@1,2,3:3,4,5#10" answer="$VoVi">
      <responseparam type="tolerance" default="0.00001"/> 
      <formulaequationinput size="40" />
    </formularesponse>

    <p>Let <i>c</i> denote the speed of light. What is the relativistic energy <i>E</i> of an object of mass <i>m</i>?</p>
  <script type="loncapa/python">
  VoVi = "(R_1*R_2)/R_3"
  </script>
    <formularesponse type="cs" samples="m,c@1,2:3,4#10" answer="m*c^2">
      <responseparam type="tolerance" default="0.00001"/> 
      <text><i>E</i> =</text> <formulaequationinput size="40"/>
    </formularesponse>

    <p>Let <i>x</i> be a variable, and let <i>n</i> be an arbitrary constant. What is the derivative of <i>x<sup>n</sup></i>?</p>
  <script type="loncapa/python">
  derivative = "n*x^(n-1)"
  </script>
    <formularesponse type="ci" samples="x,n@1,2:3,4#10" answer="$derivative">
      <responseparam type="tolerance" default="0.00001"/> 
      <formulaequationinput size="40" />
    </formularesponse>

    <!-- Example problem specifying only one variable -->
    <formularesponse type="ci" samples="x@1,9#10" answer="x**2 - x + 4">
      <responseparam type="tolerance" default="0.00001"/> 
      <formulaequationinput size="40" />
    </formularesponse>

    <solution>
      <div class="detailed-solution">
        <p>Explanation</p>
        <p>Use standard arithmetic operation symbols and indicate multiplication explicitly.</p>
        <p>Use the symbol <tt>^</tt> to raise to a power.</p>
        <p>Use parentheses to specify order of operations.</p>
      </div>
    </solution>
  </problem>

**XML 屬性資訊**

<script>


  .. image:: ../Images/formularesponse.png


<formularesponse>


  .. image:: ../Images/formularesponse3.png

Children may include ``<formulaequationinput/>``.

If you do not need to specify any samples, you should look into the use of the
Numerical Response input type, as it provides all the capabilities of Formula
Response without the need to specify any unknown variables.

<responseparam>


  .. image:: ../Images/formularesponse6.png

<formulaequationinput/>

========= ============================================= =====
Attribute                  Description                  Notes
========= ============================================= =====
size      (optional) defines the size (i.e. the width)
          of the input box displayed to students for
          typing their math expression.
========= ============================================= =====

.. raw:: latex
  
      \newpage %


圖片響應
========

The Image Response input type presents an image and accepts clicks on the image as an answer.
Images have to be uploaded to the courseware Assets directory. Response clicks are marked as correct if they are within a certain specified sub rectangle of the image canvas.

*Note The Mozilla Firefox browser is currently not supported for this problem type.*

範例問題如下：

.. image:: ../Images/image294.png
 :width: 600   


**問題代碼：**:

.. code-block:: xml

  <problem>
    <p><b>Example Problem</b></p>
  <startouttext/>
      <p>You are given three shapes. Click on the triangle.</p>
      <endouttext/>
      <imageresponse>
      <imageinput src="/c4x/edX/edX101/asset/threeshapes.png" width="220" height="150" rectangle="(80,40)-(130,90)" />
      </imageresponse>
  </problem>
  
  <problem>
      <imageresponse>
      <imageinput src="Path_to_Image_File.png" width="220" height="150" rectangle="(80,40)-(130,90)" />
      </imageresponse> 
  </problem>


**XML 屬性資訊**


<imageresponse>

  .. image:: ../Images/imageresponse1.png

<imageinput>

  .. image:: ../Images/imageresponse2.png

.. raw:: latex
  
      \newpage %


自定響應
========

A Custom Response input type accepts one or more lines of text input from the student and evaluate the inputs for correctness using an embedded Python script.

範例問題如下：

.. image:: ../Images/image295.png
 :width: 600  


**問題代碼**:

.. code-block:: xml

  <problem>
    <p><b>Example Problem</b></p>
  <script type="loncapa/python">

  def test_add_to_ten(expect,ans):
    try:
      a1=int(ans[0])
      a2=int(ans[1])
    except ValueError:
      a1=0
      a2=0
    return (a1+a2)==10

  def test_add(expect,ans):
    try:
      a1=float(ans[0])
      a2=float(ans[1])
    except ValueError:
      a1=0
      a2=0
    return (a1+a2)== float(expect)
  </script>

    <p>This question consists of two parts. </p>
  <p>First, enter two integers which sum to 10. </p>
  <customresponse cfn="test_add_to_ten">
          <textline size="40" /><br/>
          <textline size="40" />
  </customresponse>

    <p>Now enter two (finite) decimals which sum to 20.</p>
  <customresponse cfn="test_add" expect="20">
          <textline size="40" /><br/>
          <textline size="40" />
  </customresponse>

      <solution>
          <div class="detailed-solution">
              <p>Explanation</p>
            <p>For the first part, any two numbers of the form <i>n</i>
              and <i>10-n</i>, where <i>n</i> is any integer, will work. 
              One possible answer would be the pair 0 and 10.
            </p>
            <p>For the second part, any pair <i>x</i> and <i>20-x</i> will work, where <i>x</i> is any real number with a finite decimal representation. Both inputs have to be entered either in standard decimal notation or in scientific exponential notation. One possible answer would be the pair 0.5 and 19.5. Another way to write this would be 5e-1 and 1.95e1.
            </p>
          </div>
      </solution>
  </problem>

**樣板**

*With displayed suggested correct answers*

.. code-block:: xml

  <problem>

  <script type="loncapa/python">
  def test_add(expect,ans):
    a1=float(ans[0])
    a2=float(ans[1])
    return (a1+a2)== float(expect)
  </script>


  <p>Enter two real numbers which sum to 20: </p>
  <customresponse cfn="test_add" expect="20">
          <textline size="40" correct_answer="11"/><br/>
          <textline size="40" correct_answer="9"/>
  </customresponse>

      <solution>
          <div class="detailed-solution">
          </div>
      </solution>
  </problem>


**樣板**

*With NO suggested correct answers*


.. code-block:: xml

  <problem>

  <script type="loncapa/python">
  def test_add(expect,ans):
    a1=float(ans[0])
    a2=float(ans[1])
    return (a1+a2)== float(expect)
  </script>


  <p>Enter two real numbers which sum to 20: </p>
  <customresponse cfn="test_add" expect="20">
          <textline size="40" /><br/>
          <textline size="40" />
  </customresponse>

      <solution>
          <div class="detailed-solution">
          </div>
      </solution>
  </problem>


.. raw:: latex
  
      \newpage %

化學方程式響應
==============

The Chemical Equation Response input type is a special type of Custom Response
that allows the student to enter chemical equations as answers. 

範例問題如下：

.. image:: ../Images/image296.png
 :width: 600   

**問題代碼**:

.. code-block:: xml

  <problem>
    <p><b>Example Problem</b></p>
    <startouttext/>
    <p>Some problems may ask for a particular chemical equation. Practice by writing out the following reaction in the box below.</p>
    <center>\( \text{H}_2\text{SO}_4 \longrightarrow \text{ H}^+ + \text{ HSO}_4^-\)</center>
    <br/>
    <customresponse>
      <chemicalequationinput size="50"/>
      <answer type="loncapa/python">

  if chemcalc.chemical_equations_equal(submission[0], 'H2SO4 -> H^+ + HSO4^-'): 
      correct = ['correct']
  else:
      correct = ['incorrect']

  </answer>
    </customresponse>
    <p> Some tips:<ul><li>Only real element symbols are permitted.</li><li>Subscripts are entered with plain text.</li><li>Superscripts are indicated with a caret (^).</li><li>The reaction arrow (\(\longrightarrow\)) is indicated with "->".</li></ul>
     So, you can enter "H2SO4 -> H^+ + HSO4^-".</p>
    <endouttext/>
  </problem> 

.. raw:: latex
  
      \newpage %

示意圖響應
==========

The Schematic Response input type provides an interactive grid on which the
student can construct a schematic answer, such as a circuit. 

範例問題如下：

.. image:: ../Images/image297.png
 :width: 600 

.. image:: ../Images/image298.png
 :width: 600   

.. image:: ../Images/image299.png
 :width: 600   

**問題代碼**:

.. code-block:: xml


    <problem>
      Make a voltage divider that splits the provided voltage evenly.

    <schematicresponse>
    <center>
    <schematic height="500" width="600" parts="g,r" analyses="dc"
    initial_value="[["v",[168,144,0],{"value":"dc(1)","_json_":0},["1","0"]],["r",[296,120,0],{"r":"1","_json_":1},["1","output"]],["L",[296,168,3],{"label":"output","_json_":2},["output"]],["w",[296,216,168,216]],["w",[168,216,168,192]],["w",[168,144,168,120]],["w",[168,120,296,120]],["g",[168,216,0],{"_json_":7},["0"]],["view",-67.49999999999994,-78.49999999999994,1.6000000000000003,"50","10","1G",null,"100","1","1000"]]"
    />
    </center>
    <answer type="loncapa/python">
    dc_value = "dc analysis not found"
    for response in submission[0]:
      if response[0] == 'dc':
          for node in response[1:]:
              dc_value = node['output']

    if dc_value == .5:
      correct = ['correct']
    else:
      correct = ['incorrect']

    </answer>
    </schematicresponse>
    <schematicresponse>
    <p>Make a high pass filter.</p>
    <center>
    <schematic height="500" width="600" parts="g,r,s,c" analyses="ac"
    submit_analyses="{"ac":[["NodeA",1,9]]}"
    initial_value="[["v",[160,152,0],{"name":"v1","value":"sin(0,1,1,0,0)","_json_":0},["1","0"]],["w",[160,200,240,200]],["g",[160,200,0],{"_json_":2},["0"]],["L",[240,152,3],{"label":"NodeA","_json_":3},["NodeA"]],["s",[240,152,0],{"color":"cyan","offset":"0","_json_":4},["NodeA"]],["view",64.55878906250004,54.114697265625054,2.5000000000000004,"50","10","1G",null,"100","1","1000"]]"/>
    </center>
    <answer type="loncapa/python">
    ac_values = None
    for response in submission[0]:
      if response[0] == 'ac':
          for node in response[1:]:
              ac_values = node['NodeA']
    print "the ac analysis value:", ac_values
    if ac_values == None:
      correct = ['incorrect']
    elif ac_values[0][1] < ac_values[1][1]:
      correct = ['correct']
    else:
      correct = ['incorrect']
    </answer>
    </schematicresponse>

        <solution>
            <div class="detailed-solution">
                <p>Explanation</p>
                <p>A voltage divider that evenly divides the input voltage can be formed with two identically valued resistors, with the sampled voltage taken in between the two.</p>
                <p><img src="/c4x/edX/edX101/asset/images_voltage_divider.png"/></p>
                <p>A simple high-pass filter without any further constaints can be formed by simply putting a resister in series with a capacitor. The actual values of the components do not really matter in order to meet the constraints of the problem.</p>
                <p><img src="/c4x/edX/edX101/asset/images_high_pass_filter.png"/></p>
            </div>
        </solution>
    </problem>
