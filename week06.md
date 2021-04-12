
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
- Recyclerview를 이용한 게시물 보여주기
<img src="https://user-images.githubusercontent.com/29966841/114386356-14d3f180-9bcc-11eb-8730-0098ee8653c2.png" width="400">
-> recyclerview를 이용하여 데이터베이스에 있는 내용을 게시글로 보여주는 기능을 구현하려 하였다.

<img src="https://user-images.githubusercontent.com/29966841/114387845-e7884300-9bcd-11eb-8a10-e41e8fffe0bb.png" width="300">
<img src="https://user-images.githubusercontent.com/29966841/114387850-e9ea9d00-9bcd-11eb-8a31-f1a2b1206a05.png" width="300">
-> 안드로이드 스튜디오와 파이어베이스를 연결하고 데이터를 전송하는 부분까지 성공하였다.
   그러나 코드를 실행시키자 'Could not find androidx.recycleview:recycleview:1.0.0.'라는 오류 메시지가 뜨면서 실행이 되지않아 현재 해결중에있다.
