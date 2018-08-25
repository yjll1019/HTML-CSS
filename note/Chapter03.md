## Chapter03

#### 링크와 멀티미디어

1. 링크

+ 하이퍼텍스트(HyperText) : 서로 연관된 문서나 텍스트 조각들을 연결하여 원하는 정보를 찾아가도록 하는 것.

+ 하이퍼미디어(HyperMedia) : 텍스트뿐만 아니라 이미지, 그래픽, 비디오 등 멀티미디어 정보가 서로 연결되어 있는 것.

+ 노드 : HTML문서나 멀티미디어 정보를 표현하는 기본 단위.

+ 앵커(anchor)  : 노드에 해당하는 HTML문서 내에서 링크의 출발점이나 도착점.

+ &lt;a&gt;요소를 이용한 문서 간 이동.

  +  위치 지정 방법

    + 절대 속성 : http:// 로 시작하는 URL형식의 인터넷 주소 표기.

    + 상대 속성 : http://로 시작하지 않는 경우. 

      ​		현재 문서와 같은 폴더의 위치에서부터 표기된 주소로 이동.

  + ex) &lt;a href="파일이름 or URL주소" title="설명">
  + title 속성 : 하이퍼링크 위에 마우스를 가져가면 나오는 말풍선 속 설명.

+ &lt;a&gt;요소를 이용한 문서 내 특정 위치로 이동.

  + 이런한 기능의 링크를 사용하려면 목적지 앵커와 시작점 앵커를 설정해야 함.

  + &lt;a id="고유아이디"&gt; &lt;/a&gt; :  문서 내 이동할 목적지 설정.

    &lt;a href="#고유아이디"&gt; 시작점 - 링크가 설정된 '고유아이디'의 위치로 이동&lt;a&gt;

2. 이미지 사용하기

+ 이미지 파일 종류 : 웹 브라우저에서 공통적으로 사용할 수 있는 이미지 파일은 GIF, JPEG, PNG가 있음.

  +  GIF(Graphic Interchange Format) : JPEG, PNG보다 파일 크기가 작고, 자연스러운 장면을 표현하지 못함.
  + JPEG(Joint Photographic Experts Group) : 복잡한 그림, 사진 등 색상을 많이 사용하는 이미지에 적함.
  + PNG(Portable Network Graphic) : GIF와 JPEG 형식의 장점, 비압축 형식의 BMP형식의 장점도 고려함.
  + 사진과 같이 색상의 개수가 많은 이미지를 다룰 때는 JPEG 형식이 적합하고, 색상의 개수가 적거나 간단한 도형으로 이루어진 이미지를 다룰 때는 GIF가 압축률이 높음.

+ 이미지 삽입 

  + 사용할 이미지 파일을 HTML파일과 동일한 폴더 또는 하위 폴더에 저장해야함.

  + 이미지 파일이 HTML문서와 같은 폴더에 있지 않다면 src에 경로를 적어줘야함.

    ex) image파일 안에 이미지 파일이 있다면 src="image/파일이름" 의 형태로

  + ex) &lt;img src="파일이름" width="크기" height="크기" alt="대체 텍스트"&gt;

  + &lt;img&gt;요소의 alt(alternate text-대체 텍스트) 속성 

    : 이미지를 표시 못하는 경우에 대체 텍스트가 사용됨.

  + &lt;figure&gt; 요소

    + 그림, 사진, 다이어그램과 텍스트 등의 콘텐츠를 함께 묶어 하나의 독립된 단위로 취급하고 싶을 때 사용.
    + ex) &lt;figure&gt; &lt;img src="intro.jpg" alt="책표지이미지"&gt; &lt;/figure&gt;

  + &lt;figcaption&gt; 요소

    + &lt;figure&gt; 요소를 위한 제목을 표현하는 요소. figure내에 위치하면 됨.

  + &lt;figure&gt; 요소를 위한 제목을 표현하는 요소. &lt;figure&gt;내에 위치하면 됨.

+ 이미지에 하이퍼링크 연결

  + ex) &lt;a href="링크할 곳의 파일이름"&gt; &lt;img src="이미지 파일이름"&gt; &lt;/a&gt;

3. 오디오와 비디오

+ HTML5는 외부객체로 표현하지 않고 별도의 플러그인 설치없이 오디오와 비디오 재생 가능.

+ 오디오 삽입하기

  + &lt;audio controls autoplay src="재생할 사운드 파일 이름"&gt;

  + contorls 속성 : audio요소 내에 적을 시 미디어 제어기를 표시하겠다는 의미.

  + autoplay 속성 : 파일을 로드하자마자 자동으로 재생한다는 의미.

  + loop 속성 : 사운드를 반복 재생시킬 횟수를 지정.

  + 오디오 타입을 지원하지 않을 경우를 대비해서 &lt;audio&gt;요소 내의 &lt;source&gt;요소를 이용하여 같은 내용을 여러 형식으로 작성한 오디오 파일들을 지정할 수 있음.

     ex) &lt;audio controls autoplay&gt;

    &lt;source src="song.mp3" type="audio/mp3"&gt; 

    &lt;source src="song.mp3" type="audio/ogg"&gt; 	

    &lt;/audio&gt;

  + type 속성 : 오디오 파일의 MIME 형식을 지정.

    + MIME 형식 : 멀티미디어 파일에 대한 형식을 종류별로 구분하도록 한 표기.

      ex) "audio/mp3", "audio/ogg" 등

  + preload 속성 

    + auto : 웹 브라우저가 페이지를 로드하고 바로 오디오 파일 다운로드.
    + metadata : 사용자가 재생시키기 전까지는 메타데이터만 다운로드.
    + none : 사용자가 재생을 시작하기 전까지는 파일을 다운로드 하지 않음.

+ 비디오 삽입하기

  + &lt;video controls src="재생할 비디오 파일 이름" width="폭" height="높이"&gt;
  + src, controls, loop, autoplay 속성은 &lt;audio&gt; 요소의 속성들과 동일.
  + width, height 속성 : 비디오 콘텐츠가 표시될 영역의 크기를 설정. 비디오 자체의 크기와 일치하지 않을 경우 비디오 콘텐츠가 늘어나거나 잘릴 수 있음.
  + videoWidth, videoHeight : 비디오 자체의 너비, 높이를 반환하는 속성.
  + poster : 비디오가 로딩되고 있을 때 보여줄 이미지를 지정하는 속성.
  + preload : 브라우저가 미리 동영상을 로딩할지 지정하는 속성. (&lt;audio&gt;와 동일)
    + 속성이 metadata인 경우 비디오의 첫 프레임이 나타남.

4. 객체 포함하기 

+ HTML 문서에서는 다른 HTML파일이나 이미지, 멀티미디어 파일 등 외부 객체를 포함할 수 있음.
+ &lt;iframe&gt;  요소 : 새로운 브라우저로 이동하지 않고 한 화면에서 링크로 연결된 내용을 같이 볼 수 있음.
  + &lt;iframe&gt;의 속성
    + src : 파일의 url 지정.
    + width, height : 삽입될 브라우저 프레임의 가로와 높이의 크기 지정.
    + name : 브라우저 프레임의 이름 지정.
    + &lt;a&gt;요소의 target속성에 &lt;iframe&gt;의 이름을 지정하면 링크를 클릭할 때 연결된 문서가 내부 프레임에 나타남.
  + ex) &lt;iframe src="내부 프레임에 출력할 파일의 URL" width="폭" height="높이" name="이름"&gt; &lt;/iframe&gt;
+ &lt;embed&gt; 요소 
  + &lt;iframe&gt;와 마찬가지로 src, width, height의 속성을 가짐.
  + ex) &lt;embed src="삽입할 파일의 URL" width="폭" height="높이"&gt; 
+ HTML5는 XML과 호환되기 때문에 XML로 작성된 문서를 웹 페이지에 바로 포함시킬 수 있음.
  + &lt;canvas&gt;요소로 그림 그리기
  + &lt;svg&gt;요소로 벡트 그래픽스 그리기
  + &lt;math&gt;요소로 수학 공식 표현하기