## CHATER02

#### HTML문서의 기본

+ <!DOCTYPE html> : 문서의 종류를 알리기 위한 선언

+ HTML문서의 요소는 내용과 이를 둘러싼 태그로 이루어져있다.

+ 태그의 이름에서 대소문자를 구분하지 않는다.

+ 단독태그 : <태그이름 /> - 시작 태그에서 태그이름 뒤에 /를 표시하면 종료태그를 작성하지 않아도 된다. ex) [br /] , [img /], [hr /]

+ 속성(Attribute) : 요소에 추가정보를 주기 위해서 사용한다. 각 속성은 빈칸으로 구분된다.

  <이름 = "속성값"> 의 형태로 작성된다. ex) [a href="ch02.html" target="blank"]

+ html문서는 head와 body요소로 구성되어 있다.

+ 특수문자 표기 시 &이름; 형식으로 표기한다.

  + 주요 특수 문자
    + 공백 문자 : & nbsp;
    + '<' : & lt;
    + '>' : & gt;
    + " : & quot;
    + & : & amp;

+ head 요소 

  + title 요소 - 제목을 적어놓는 요소.

  + meta 요소 - 문서 관리를 위한 메타정보를 나타내는 요소.

    : 문서 자체에 대한 정보나 키워드, 문자 인코딩 정보, 저자 정보 등

    ex) meta name="authors" content="이예지"

    ​     meta charset="utf-8"

+ 문자 인코딩 UTF-8과 EUC-KR

  + UTF-8(유니코드) : 현대 한글뿐 아니라 한글 고어, 각종 외국 언어의 문자 처리 가능.
  + ECU-KR(완성형코드) : 현대 한글 중 완성형 코드에 있는 문자만 표현 가능. UTF-8보다 표현할 수 있는 문자가 적다.

+ 설명문(Comment)

  : 소스코드 이외에 코드에 대한 설명, 정보를 기록할 때 사용한다. ''<!-- 설명 -->" 

+ 문서 내용을 표현하는 다양한 요소들

  + 제목(Headline) &lt;h1&gt;~&lt;h6&gt; 
  + 단락(Paragraph) &lt;p&gt;
  + 줄 바꿈(Link Break) &lt;br&gt;
  + 가로줄(Horizontal Line) &lt; hr&gt;
  + 작성된 형식 유지(Pre-formatted Text) &lt;pre&gt;
  + 단락 인용(Block Quotation) &lt;blockquote&gt;

+ 다양한 텍스트 표현들

  + <em>텍스트 강조(Emphasis)</em> &lt;em&gt;

  + <strong>강한 강조(Strong Emphasis)</strong> &lt;strong&gt;

  + <small>작은 글자</small> &lt;small&gt;

  + <mark>하이라이트(Marked) 효과</mark> &lt;mark&gt;

  + <sup>위 첨자(Superscript)<sup> &lt;sup&gt;

    <sub>아래 첨자(Subscript)<sub> &lt;sub&gt;

+ HTML5문서 규약에서는 가급적 문서의 출력 모양은 CSS를 사용하여 표현하는 것을 권장한다.

+ 목록 나열하기

  + 순서가 없는 목록(Unordered List) : &lt;ul&gt; 후 안에 &lt;li&gt; 요소 포함시켜야한다.

  + 순서가 있는 목록(Ordered List) : &lt;ol&gt; 후 안에 &lt;li&gt; 요소 포함시켜야한다.

  + 설명 목록(Description List 혹은 Definition List) : &lt;dl&gt;

    : &lt;dl&gt;요소 내에 설명하고자 하는 용어는 &lt;dt&gt;에 적고, 그 설명은 &lt;dd&gt;에 적어야한다.

+ 표 작성하기

  + &lt;table&gt;

    &lt;tr&gt;

     &lt;th&gt;제목&lt;/th&gt;

    &lt;/tr&gt;

    &lt;tr&gt;

    &lt;td&gt;내용&lt;/td&gt;

    &lt;/tr&gt;

    &lt;/table&gt;

+ 표의 구조적 표현

  + 셀 합치기

    + &lt;td rowspan="3"&gt; 아래 줄 3개의 셀을 합치겠다.
    + &lt;td colspan="3"> 옆 칸의 3개의 셀을 합치겠다.

  + 표를 설명하는 제목 입력 &lt;caption&gt;

  + 표의 머리줄, 몸체, 꼬리줄 표현 &lt;thead&gt;, &lt;tbody&gt;, &lt;tfoot&gt;

    : 표의 길이가 클 경우 머리줄과 꼬리줄을 고정한 채 몸체만 스크롤하는 것이 가능하다.

+ 웹문서 구조화 요소

  : 컴퓨터에게 문단에 대한 의미를 정확하게 지정해주기 위한 요소들로써, 화면상으로는 모양이 구분되어 표시되지 않는다.

  + 머리말 &lt;header&gt; : 웹 문서에서 페이지 혹은 섹션의 머리말 영역을 나타낼 때 사용.

  + 탐색 &lt;nav&gt; : 내비게이션 링크(<small>웹 문서의 한 지점에서 다른 웹문서나 문서 내의 다른 부분으로 이동하는 것.</small>)를 표현할 때 사용.

  + 독립된 본문 &lt;article&gt; : 하나의 신문안에 여러 개의 기사처럼 독립된 본문을 나타낼 때 사용. header, footer, section요소가 포함될 수 있음.

  + 문서내 섹션 그룹 &lt;section&gt; : 웹문서 내에서 절 단위로 구분하거나 의미가 비슷한 그룹으로 문서를 구분하여 묶기 위해서 사용.

  + 부수 정보 &lt;aside&gt; : 본문의 내용과 구별되는 별개의 정보를 표현하기 위해 사용.

  + 꼬리말 &lt;footer&gt; : 웹 문서에 꼬리말에 해당하는 저자 정보, 이용조건, 관련 링크 등을 나타내기 위해 사용.

     