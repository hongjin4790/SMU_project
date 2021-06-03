# SW(Sangmyung 友) 
<p align="center">
<img width="400px" src="https://user-images.githubusercontent.com/29851772/120697106-468c7900-c4e8-11eb-9b9f-0e5a608e5bfc.png">
  
</p>

<!-- TABLE OF CONTENTS -->
<details open="open">
  <summary>Table of Contents</summary>
  <ol>
    <li>
      <a href="#어플-소개">어플 소개</a>
      <ul>
        <li><a href="#환경-설정">환경 설정</a></li>
      </ul>
    </li>
    <li>
      <a href="#본문">본문</a>
      <ul>
        <li><a href="#로고-의미">로고 의미</a></li>
        <li><a href="#주요-기능-설명">주요 기능 설명</a></li>
        <li><a href="#영상">영상</a></li>
      </ul>
    </li>
    <li><a href="#앱-다운로드-링크">앱 다운로드 링크</a></li>
  </ol>
</details>

## 어플 소개
SW는 (Sangmyung 友) 코로나 시국에 비대면으로 하는 수업이 많아지다보니 신입생들은 동기들과 친해지는데 어려움이 있고
<br>학교나 본인 학과에 대한 정보를 얻기도 힘들고 아는 사람이 없어 혼밥 하는 학생들도 많습니다. 
<br>이를 해소하기 위해 학교 학생들끼리 편하게 교류 할 수 있는 여러 기능이 구현 되어 있는 어플 입니다. 

 <h3>환경 설정</h3>

     Android Studio
       - 에뮬레이터로 실행 시 Pixel 4 XL 사용 권장
         화면이 작은 기기로 실행 시 디자인 일그러지는 부분 발생

  
## 본문
 <h3>로고 의미</h3>
  
 저희 로고는 상명대학교와 친구를 의미하는 ‘友 벗 우’를 합친 슴우라 하여 영어로 SW입니다.
  
 <h3>주요 기능 설명</h3>
 
### 회원정보 입력
회원가입 후 이메일 인증을 완료하면 회원정보를 입력할 수 있는 액티비티가 나온다.


<img width="30%" height = "30%"  src="https://user-images.githubusercontent.com/79888537/120705692-1b5b5700-c4f3-11eb-994a-3edb0a2754cd.gif">
이름과 주소, 전화번호, 생년월일은 EditText밑에 정해진 숫자 범위를 넘어가면 빨간불이 들어온다. 
이는 정해진 문자열 길이가 초과했다는 것을 의미한다. 만약 잘못 입력했다면 EditText 오른쪽 맨끝에 버튼을 눌러
입력했던 값을 다 지워줄 수 있다.



<img width="30%" height = "30%"  src="https://user-images.githubusercontent.com/79888537/120705698-1e564780-c4f3-11eb-9261-bd3888188fbe.gif">
만약 저 범위를 벗어난채로 회원정보 등록을 하면 
글자수가 너무 길다는 토스트 메세지가 나오게 된다. 



<img width="30%" height = "30%"  src="https://user-images.githubusercontent.com/79888537/120705707-21513800-c4f3-11eb-8045-43356da01620.gif">
또한 빈칸이 존재한 채로 회원정보 등록 버튼을 누르게 되면 빈칸을 입력하라는 토스트 메세지가 뜬다.



### 회원정보 수정
<img width="30%" height = "30%"  src="https://user-images.githubusercontent.com/79888537/120705755-2dd59080-c4f3-11eb-808b-0d0c130325ce.jpg">
회원가입하고 등록했던 정보들을 확인할 수 있는 액티비티이다. 메인엑티비티 우측 최상단 사람 모양 아이콘을 
클릭하면 들어갈 수 있다. 이곳은 그림과 같은 디자인을 하고 있다.



<img width="30%" height = "30%"  src="https://user-images.githubusercontent.com/79888537/120705780-362dcb80-c4f3-11eb-9e6d-bcc7ce47c8db.gif">
회원정보중에 수정할 수 있는 데이터는 전화번호, 주소, 학과를 변경 할 수 있다. 변경을 원하면  해당 텍스트뷰 
오른쪽에 수정버튼을 클릭하면 수정할 데이터를 넣을 수 있는 EditText가 나오게 된다. 이곳에 데이터를 집어넣고
정보수정을 누르면 수정을 원하는 부분만 바꿀 수 있게 된다.

### 게시판

어플 내 게시판은 '학과 게시판' ,'학교 게시판' 두가지로 나뉩니다.

<img width="30%" height = "30%" alt="채팅" src="https://user-images.githubusercontent.com/29966841/120702452-0da3d280-c4ef-11eb-82ea-b51aa76cc468.jpg"><img width="30%" height = "30%" alt="채팅" src="https://user-images.githubusercontent.com/29966841/120702563-31671880-c4ef-11eb-9f98-fba3d69e435a.jpg">

'학과 게시판'은  회원가입시 설정한 학과가 같은 이용자들 끼리만 사용할 수 있는 게시판입니다.<br/>
'학교 게시판'은 학과 상관없이 모든 학교 학생들이 사용할 수 있는 게시판입니다. 







### 인앱 결제

- Google Console에 들어가 개발자 등록을 먼저 해준다 ($25 1회 최초 등록을 해야한다.)


### 라이센스 테스트

결제 리스트를 할 때, 실제 돈이 빠져나가지 않도록 해야하기 때문에 라이센스 테스트를 신청해야한다.

구글 플레이 콘솔 > 설정 > 라이센스 테스트에 라이센스 

테스터를 등록하면 아이디로 결제하는 건은

테스트 건으로 처리되어 실제 돈이 청구되지 않는다. 

-라이센스 테스트

<img width = "55%" height ="55%" src = "https://user-images.githubusercontent.com/79883776/120706077-9e7cad00-c4f3-11eb-8635-9e80e3fe3830.png">

### 앱 만들기

구글 플레이 콘솔에서 앱을 만듭니다.

-[내부 테스트 설정]

앱에 있는 apk 파일을 업로드하고 테스터를 지정하면, 등록한 이메일을 사용하는 

Google Play 이용자는 내부 테스트를 진행 할 수 있게 됩니다.

### 인앱상품

APK가 업로드되면 수익창출 > 제품 > 인앱상품 순으로 들어가 

어플리케이션에서 사용할 아이템을 만들어 줍니다.

<img width = "65%" height ="65%" src = "https://user-images.githubusercontent.com/79883776/120707555-71c99500-c4f5-11eb-8d5c-e1a760ca4eb3.JPG">

(단, 인앱상품의 id를 지정해줄때 android studio의 MarketFragment에 있는 id값과 같게 해야함. )

 다이아몬드 세개 올린 인앱상품 사진

<img width = "30%" height ="30%" src = "https://user-images.githubusercontent.com/79883776/120707098-df28f600-c4f4-11eb-81d1-aa3425e6e430.gif">





 <h3>영상</h3>
  
  
  
  
  //유튜브 링크
  

  
  
## 앱 다운로드 링크

  // SMU 깃허브 링크

  
  
  
  
  
  
  
  
  
  
  
  
  
  
