# WEEK 12

### <랜덤매칭 기능 구현>

- 어플리케이션 실행시 메인화면 

-> 어플을 실행하게 되면 메인화면이 보여지고 '관심사 설정' 버튼과 '친구 찾기' 버튼을 확인할 수 있다.

<img width="30%" src="https://user-images.githubusercontent.com/29966841/119364356-c5fc9a00-bce9-11eb-92be-e771d206f360.png"/>

- 랜덤매칭을 위한 매칭조건 설정화면

-> '관심사 설정' 버튼을 누르면 사용자가 어떤 조건으로 랜덤매칭을 진행할 것인지 설정할 수 있는 화면이 보여지고, 매칭 조건을 설정할 수 있다.

<img width="30%" src="https://user-images.githubusercontent.com/29966841/119365124-95693000-bcea-11eb-9373-992a8b82e794.png"/>

- 같은 조건이 설정된 사용자들끼리 매칭 진행

-> 아래의 데이터베이스 화면을 보면 '2대2' 매칭조건을 선택하고, '친구 찾기' 버튼을 누른 사용자들의 UID가 데이터베이스에 들어오는 것을 볼 수 있다. 
   '2대2' 매칭의 인원수는 4인이기 때문에 4명의 UID가 db에 들어와야 매칭이 실행된다.

<img width="50%" src="https://user-images.githubusercontent.com/29966841/119371847-bb460300-bcf1-11eb-8c49-8f43844101bc.png"/>

- 매칭 완료 시

-> 

<img width="30%" src="https://user-images.githubusercontent.com/29966841/119374240-4e803800-bcf4-11eb-8758-d9bb8bfa8085.png"/>
