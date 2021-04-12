
# WEEK 06

### 김홍진
- 이메일 인증
1. 이메일로 회원가입을 하면 가입을 한 이메일로 인증메일이 간다. 인증을 하면 다음으로 회원정보를 입력해야한다. 입력을 하면 DB에 내 정보가 저장이 된다.
<img width="632" alt="이메일인증" src="https://user-images.githubusercontent.com/29851704/114301396-9b6ecd00-9aff-11eb-8daa-c33e7cb04a67.PNG">

- 채팅기능 구현
<img width="185" alt="채팅창" src="https://user-images.githubusercontent.com/29851704/114301487-1df78c80-9b00-11eb-8ab8-f96211175cc6.PNG">
1. 회원정보를 입력하면 DB에 저장이 된다.
<img width="234" alt="DB내저보 저장" src="https://user-images.githubusercontent.com/29851704/114301549-4da69480-9b00-11eb-8f53-e592aec8de22.PNG">
2. 서로 채팅을 하면 채팅한 내용들이 실시간으로 DB에 저장되고 저장된 값을 읽어오는 방법으로 구현했다.
<img width="175" alt="채팅내용" src="https://user-images.githubusercontent.com/29851704/114301590-762e8e80-9b00-11eb-85a2-283b0de2e8f2.PNG">

### 정지원
#### - Recyclerview를 이용한 게시물 보여주기
<img src="https://user-images.githubusercontent.com/29966841/114386356-14d3f180-9bcc-11eb-8730-0098ee8653c2.png" width="400">
-> recyclerview를 이용하여 데이터베이스에 있는 내용을 게시글로 보여주는 기능을 구현하려 하였다.

<img src="https://user-images.githubusercontent.com/29966841/114387845-e7884300-9bcd-11eb-8a10-e41e8fffe0bb.png" width="300">
<img src="https://user-images.githubusercontent.com/29966841/114387850-e9ea9d00-9bcd-11eb-8a31-f1a2b1206a05.png" width="300">
-> 안드로이드 스튜디오와 파이어베이스를 연결하고 데이터를 전송하는 부분까지 성공하였다.
<img src="https://user-images.githubusercontent.com/29966841/114388652-f02d4900-9bce-11eb-95b8-28175bb33c81.png" width="400">
그러나 코드를 실행시키자 'Could not find androidx.recycleview:recycleview:1.0.0.'라는 오류 메시지가 뜨면서 실행이 되지않아 현재 해결중에있다.

#### - 게시판 구현
<img src="https://user-images.githubusercontent.com/29966841/114389922-93329280-9bd0-11eb-92ca-b7f8a6b09c74.png" width="300">
-> 그림과 같은 형태의 게시판을 구현하는것을 목표로 파이어베이스와 연동하여 게시판을 만들어보았다.
<img src="https://user-images.githubusercontent.com/29966841/114390480-4dc29500-9bd1-11eb-9d94-210610158df6.png" width="400">
-> 위의 사진과 같이 목표한 형태로 게시판을 구현하였고 파이어베이스와 연결도 성공하였다.
<img src="https://user-images.githubusercontent.com/29966841/114391020-efe27d00-9bd1-11eb-9319-16f771428bb1.png" width="400">
그러나 프로젝트를 실행시키는 과정에서 오류가 발생하여 해결하는 과정에 있다.


### 황의혁

1. 어플 누른 후 
   1-1) 상명대 로고의 이미지 나옴.

2. 로그인 창이 나옴 
   2-1) 로그인 창 + 회원가입란

3. 회원가입 
   3-1) 회원가입시 이메일 인증 필요

4. 로그인 후 기능 별로 버튼을 추가함 (메인 기능)
   4-1) 기능1 : 랜덤 채팅 세부 기능- 랜덤채팅이 매칭 될 시 채팅 가능(서버 구축) 
   4-2) 기능2 : 자기만의 스케줄 등록
   4-3) 기능3 : 추가.

5. 메인 기능을 누르면 세부 기능 창으로 넘어간다.
   5-1) 세부기능 창에서 네이게이션 바를 이용해 검색, 자기정보 등을 찾을 수 있게한다.  
   
### 한창훈

기본적인 디자인이 만들어지기 전까지 어플에서 유용하게 쓰일 기능 공부
안드로이드 스튜디오 관련 책과 구글, 유튜브를 통한 학습

위에 조원이 디자인한 메인 기능을 누르면 세부기능 창으로 넘어가고 세부기능 창에서 네비게이션 바를 통해 검색,
자기정보를 찾을 수 있게하는 레이아웃을 네비게이션바, 리스트뷰, 카드뷰 등을 이용해 구현중에 있다.


