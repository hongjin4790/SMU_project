# WEEK 11

<김홍진>

저번주에 댓글을 쓰면 댓글을 쓴 사용자의 데이터를 불러오지 못하는 오류가 있었다. 이 오류를 해결하기 위해서 DB에 저장되는 구조를 변경을 해서 해결을 할 수 있었다.

![학과나눈게시판](https://user-images.githubusercontent.com/29851704/118490956-7b16db80-b759-11eb-8946-795e5c7bede4.PNG)

아래의 사진은 여러 사용자가 댓글을 쓰고 데이터가 정상적으로 오는 것을 볼 수 있다.

![저번주오류](https://user-images.githubusercontent.com/29851704/118491295-ccbf6600-b759-11eb-9ec3-ba05bb791070.PNG)

이번주에는 회원가입을 하고 사용자의 정보를 입력할 때 소속된 학과와 성별을 체크할 수 있도록 추가했다.

![캡처](https://user-images.githubusercontent.com/29851704/118490952-79e5ae80-b759-11eb-88a6-81320d906fc1.PNG)

그리고 학생들이 다 볼 수 있는 학교게시판을 만들었다. 아래의 사진은 학교게시판의 DB 구조이다.

![학교게시판](https://user-images.githubusercontent.com/29851704/118490945-78b48180-b759-11eb-8868-9f533c9b7bdc.PNG)


<한창훈>
지난번 파이어베이스에서 안드로이드 스튜디오로 데이터를 가져오는 과정에서 오류가 발생했고 이를 해결했다. 이번주에는 그 후 작업들을 진행하였다.

먼저 내정보 화면이다. 이 화면에서는 내가 회원가입하고 난 후 입력했던 이름,전화번호, 주소, 학과, 성별이 나오게 된다. 내정보 화면에서 회원탈퇴를 누르게 되면 자신이 가입했던 모든 정보들이 삭제된다.
<img width="40%" src="https://user-images.githubusercontent.com/79888537/118497364-f7142200-b75f-11eb-8ba6-d98f0795be84.png"/>

위에 화면에서 수정이 필요하면 전화번호, 주소, 학과를 연필버튼을 눌러 EditText가 나오게 한다. 여기서 수정하고 싶은 정보를 입력하면 정보가 바뀌게 된다. 아래와 같이 주소에 Seoul을 입력하고 수정버튼을 누르게 되면 데이터베이스에 있는 값도 자동으로 바뀌게 되고 내정보화면에 값도 업데이트가 된다.
<img width="40%" src="https://user-images.githubusercontent.com/79888537/118498092-9fc28180-b760-11eb-953a-838c2baa2279.png"/>
<img width="40%" src="https://user-images.githubusercontent.com/79888537/118498541-18c1d900-b761-11eb-9534-14b4478f9d63.png"/>
<img width="40%" src="https://user-images.githubusercontent.com/79888537/118498274-d3051080-b760-11eb-9079-bebe908ef5f9.png">
<img width="40%" src="https://user-images.githubusercontent.com/79888537/118498288-d5676a80-b760-11eb-8276-ecb19ade8d9a.png">

기본적인 회원정보를 수정할 수 있을 뿐만 아니라 비밀번호 재설정도 할 수 있다. 여기서 자신이 원하는 비밀번호를 입력하고 재설정을 누르면 바뀌게 된다.
<img width="40%" src="https://user-images.githubusercontent.com/79888537/118498786-59b9ed80-b761-11eb-8eed-3b3f8cd688f0.png">



<황의혁>

결제 시스템이 잘 작동 하는지 확인하기 위해 모의 앱을 만들어 실험해봤다.
<img width = "50%" src ="https://user-images.githubusercontent.com/79883776/118503788-e8c90480-b765-11eb-91d7-226c34ac329a.png"/>

인앱 상품에 두 상품을 등록시켜준다.

<img width = "50%" src = "https://user-images.githubusercontent.com/79883776/118506088-faaba700-b767-11eb-95af-af27679ecf1e.png"/>


일단 처음 화면은 한 번 구매하면 계속 사용할 수 있는 아이템과, 그 밑은 일회성 아이템이다.

<img width ="40%" src ="https://user-images.githubusercontent.com/79883776/118505237-342fe280-b767-11eb-823e-32f60a0861ff.jpg"/>

한 번 구매하면 계속 사용할 수 있는 아이템을 눌러보겠다.!

<img width ="40%" src="https://user-images.githubusercontent.com/79883776/118505302-43af2b80-b767-11eb-8bd4-11b70ed5e317.jpg"/>

그다음 결제 버튼을 누르면

<img width ="40%" src ="https://user-images.githubusercontent.com/79883776/118505360-4e69c080-b767-11eb-8f2a-8a6c715b1103.jpg"/>


결제 완료가 나타난다.




