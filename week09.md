# WEEK 09

## <Week9 활동내용>
### 황의혁
<인앱 결제 방식- 수익화 방안>

1. 광고 차단입니다.

광고 차단은 한 번만 구매하면 평생 사용할 수 있습니다. 만약 당신이 만든 어플의 기능이 뛰

어나지만 광고를 붙여 놓는다면 고객의 선택은 세 가지 중 하나입니다. 광고를 보고 쓰거나, 

어플을 지우거나, 광고 제거를 위해 돈을 쓰거나 중 하나가 됩니다.

하지만 무분별한 광고 차단 유도 결제는 사용자의 거부감을 일으킬 수 있으므로 보류중에 있

습니다. 

2. 채팅 수 제한을 시킨 후 가상화폐나 결제를 해야 만 더 대화를 이어갈 수 있습니다.

수익의 구조는 랜덤 매칭(랜팅,밥팅) 이 성사되고 서로의 채팅이 성사될 시 

채팅의 횟수를 제한하고 제한된 횟수에 도달 시 가상의 화폐 또는 현금으로 결제를 하여야

대화를 더 이어갈 수 있도록 했습니다.

<결제등록방법> 

Google play console에 들어가서 등록해야 합니다.

등록 후 그 안에 있는 Google play console에 안에 있는 check box들을 구체적으로 채워 

줘야 합니다. 개발자 등록할 시 => 이러한 문구가 나옴

*계정을 만들려면 등록 수수료 25달러를 1회 결제해야 합니다. 계정 등록을 완료하기 위해 유

*효한 신분증을 사용하여 본인 인증을 진행하라는 메시지가 표시될 수 있습니다. 본인 여부를 

*확인할 수 없는 경우 등록 수수료는 환불되지 않습니다.

과정 중 비용이 발생하는 부분이 생겨서 교수님께 여쭤보고 실행할 생각입니다.

-----------------------------------------------------------------------------------------------------------------------------------------------------------

### 김홍진

<게시판 분류 및 게시물 목록 구현>

![학교게시판](https://user-images.githubusercontent.com/29851704/116882130-09ba3180-ac5f-11eb-83e0-544406d66801.PNG)

![과 게시글](https://user-images.githubusercontent.com/29851704/116882141-0cb52200-ac5f-11eb-81d7-1c465a01188d.PNG)

<게시글 쓰기 및 새로고침 구현>

<img width="30%" src="https://user-images.githubusercontent.com/29851704/116882885-ec399780-ac5f-11eb-91ba-9f7ba7e93420.gif"/>

-----------------------------------------------------------------------------------------------------------------------------------------------------------

### 안세준

<img src="https://user-images.githubusercontent.com/29851772/116883515-a8935d80-ac60-11eb-948a-e388461305a5.gif" width="300">

 - 매칭 화면 구현 
 - 어플의 핵심 기능인 매칭 화면을 구현하였는데 화면 크기에 따라 이미지가 일그러지는 현상이 생겨서 고쳐보려고 노력중이다.

<img src="https://user-images.githubusercontent.com/29851772/116888791-d54a7380-ac66-11eb-9979-060ab853e8cb.png" width="300">

 - navigation bar를 이용하여 fragment 전환하는 형식으로 구조 변경 
 - 이전 버전에서 버튼과 네비게이션바가 겹치는 부분을 제거하고 깔끔하게 변경

-----------------------------------------------------------------------------------------------------------------------------------------------------------

### 한창훈
프레그먼트와 하단 네비게이션바르 구현하였다.

1. 한끼, 게시판과 같이 게시판을 누르게 되면 두번째 사진과 같이 선택된 버튼에 프레그먼트가 홈화면에 표시 된다.
<img width="30%" src="https://user-images.githubusercontent.com/79888537/116883894-117ad580-ac61-11eb-98c0-ee92b21c9917.png"/>  
<img width="30%" src="https://user-images.githubusercontent.com/79888537/116883739-e5f7eb00-ac60-11eb-9055-ba868874d90c.png"/>

2. 하단 네비게이션바르 누르면 게시판, 채팅과 같이 그에 맞는 화면이 fragment로 표시되게 된다.
<img width="30%" src="https://user-images.githubusercontent.com/79888537/116884125-56067100-ac61-11eb-965d-2c0b206a6405.png"/>  
<img width="30%" src="https://user-images.githubusercontent.com/79888537/116884141-5acb2500-ac61-11eb-85fd-357c5e28e361.png"/>

3. 만약 메인 버튼화면에서 게시판을 누르게 되며 네비게이션바에 home에 게시판이 오게된다. 게시판이 home으로 가고 원래 게시판이 있던 자리엔 한끼메뉴를 넣었다.
<img width="30%" src="https://user-images.githubusercontent.com/79888537/116885029-61a66780-ac62-11eb-94b0-b4e012bbea59.png"/> 
<img width="30%" src="https://user-images.githubusercontent.com/79888537/116885042-666b1b80-ac62-11eb-9ab4-40056a853058.png"/>

=> 하지만 이렇게 할 경우 메인엑티비티와 하단 네비게이션바가 중복되는 기능이 생기게 된다. 이 문제를 해결하기 위해 어플리케이션 실행 구조를 바꾸었다. 자세한 내용은 위에있는 <week 09 회의내용>에 나와있다.

-----------------------------------------------------------------------------------------------------------------------------------------------------------

### 정지원
<조건설정 및 조건에 맞는 사용자 랜덤매칭 후 채팅방생성>

- 코드 실행화면

<img src="https://user-images.githubusercontent.com/29966841/116911457-e0f76380-ac81-11eb-93a8-82511ad6a8c2.png" width="200">

-> '매칭시작' 부분을 클릭하게 되면 비슷한 관심사를 가진 사용자들과 매칭되게 된다.

<img src="https://user-images.githubusercontent.com/29966841/116911814-4c413580-ac82-11eb-90f8-b1756976adfd.png" width="200">

-> 매칭이 완료되면 채팅방이 만들어지고, 상대방과 채팅을 진행할 수 있다. 말풍선 아래에는 채팅을 읽지않은 상대방의 숫자와 채팅을 보낸 시간이 보여진다.

<img src="https://user-images.githubusercontent.com/29966841/116912228-e86b3c80-ac82-11eb-814a-242383bfbf5c.png" width="200">

-> 매칭되어 생성된 채팅방 목록들을 보여준다.

- 오류
<img src="https://user-images.githubusercontent.com/29966841/116912560-5879c280-ac83-11eb-9c4e-70a840f18939.png" width="500">

<img src="https://user-images.githubusercontent.com/29966841/116912571-5b74b300-ac83-11eb-82ca-2cfd9338b190.png" width="500">

-> gradle.properties에 주석을 추가해줬는데도 package에 주석이 존재하지 않는다는 오류가 발생하여 현재 해결중에 있다.

-----------------------------------------------------------------------------------------------------------------------------------------------------------

## <Week9 회의 내용>
#### - 각 팀원별 담당파트 진행에 필요한 어플리케이션 구조 세분화 및 조정

1. 어플리케이션 실행 구조 변경 : 기존에 로그인 후 버튼 클릭을 통해 레이아웃을 이동하였는데, 불필요하다 판단되어 로그인 후 바로 랜덤매칭 레이아웃으로 이동하도록 조정
    
    어플리케이션 실행 -> 로딩화면 -> 로그인화면 -> 랜덤매칭 화면(메인레이아웃)
   
2. 게시판 엑티비티

   - 학교전체 게시판 / 학과 게시판 분류
   - 게시물 작성, 게시물 목록 보여주기(구현)
   - 게시물 수정, 삭제 기능 구현예정
 
3. 랜덤매칭 액티비티

   - 랜덤채팅은 1:1 / 2:2 / 3:3 으로 분류
   - 밥친구매칭은 2명 / 3명 / 4명으로 분류
   - 사용자의 선택에 따라 매칭 후 채팅방 생성

4. 어플리케이션 부가기능

   - 내정보(개인정보 수정, 회원탈퇴 등)
   - 채팅방 내 읽음/안읽음 표시, 어플 알림기능, 신고기능
   - 충전 및 결제기능 

5. 팀 활동 역할분담
   - 내정보(개인정보 수정, 회원탈퇴 등) : 한창훈
   - 채팅방 내 읽음/안읽음 표시, 어플 알림기능, 신고기능 : 안세준
   - 충전 및 결제기능 : 황의혁
   - 랜덤매칭 : 정지원
   - 게시판 : 김홍진

