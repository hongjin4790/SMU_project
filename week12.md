# WEEK 12

### <랜덤매칭 기능 구현완료>

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

-> 아래 화면을 보면 '2대2' 매칭 조건을 설정한 4명의 사용자의 UID가 화면에 보여지고 있다. 
   또한 짜여진 코드에 의해 매칭이 완료되는 순간 데이터베이스에서 매칭된 사용자의 UID가 삭제되게 된다.

<img width="30%" src="https://user-images.githubusercontent.com/29966841/119374240-4e803800-bcf4-11eb-8758-d9bb8bfa8085.png"/>

<매칭조건 설정을 통한 랜덤매칭 코드구성>

    class TimeThread extends Thread{
        @Override
        public void run() {
        
            while(isReady)
            {
                try {
                    matchingMember();
                    sleep(1000);
                    Log.d( "사이즈: ", String.valueOf(matchedUidArrayList.size()));
                    
                    if(matchedUidArrayList.size() == 2 && Storage.MyInterest.equals("1대1") ) // 관심사 2인 선택
                    {
                        isReady=false;
                        
                        //uid intent로 보내줌
                        Activity root = getActivity();
                        Intent intent = new Intent(root,MessageActivity.class);
                        intent.putStringArrayListExtra("destinationUid",matchedUidArrayList);
                        startActivity(intent);
                        
                        matchedUidArrayList.clear();
                    }
                    
                    else if(matchedUidArrayList.size() == 4 && Storage.MyInterest.equals("2대2"))
                    {
                        isReady=false;
                        
                        Activity root = getActivity();
                        Intent intent = new Intent(root,MessageActivity.class);
                        intent.putStringArrayListExtra("destinationUid",matchedUidArrayList);
                        startActivity(intent);
                        matchedUidArrayList.clear();
                        sleep(1000);
                        
                        matching_removeUser(); // 매칭이 완료되면 사용자 UID 삭제
                    }
                    
                    else if(matchedUidArrayList.size() == 3 && Storage.MyInterest.equals("3인"))
                    {
                        isReady=false;
                        
                        Activity root = getActivity();
                        Intent intent = new Intent(root,MessageActivity.class);
                        intent.putStringArrayListExtra("destinationUid",matchedUidArrayList);
                        startActivity(intent);
                        matchedUidArrayList.clear();
                        sleep(1000);
                        
                        matching_removeUser();
                    }
                    
                    else if(matchedUidArrayList.size() == 2 && Storage.MyInterest.equals("2인"))
                    {
                        isReady=false;

                        Activity root = getActivity();
                        Intent intent = new Intent(root,MessageActivity.class);
                        intent.putStringArrayListExtra("destinationUid",matchedUidArrayList);
                        startActivity(intent);

                        matchedUidArrayList.clear();
                    }
                }catch (InterruptedException e){
                    e.printStackTrace();
                }
            }
        }
    }


### <이후 프로젝트 진행계획>
1. 매칭완료 후 매칭된 사용자들끼리의 채팅방 생성해주는 기능 구현
2. 어플리케이션의 전반적인 디자인 마무리
3. 회원가입시 자신의 학과를 선택하는 부분에서 '휴대폰 카메라 글자인식'을 통한 자신의 학과 인증기능 추가

- 일자별 프로젝트 세부 진행계획표

날짜 | 진행내용
:----: | ----
5/25 ~ 5/30 | 매칭후 채팅방생성 기능 구현 및 '카메라 글자인식'을 통한 학과인증기능 구현
5/31 ~ 6/6 | 어플리케이션 내 오류수정 및 디자인 마무리
6/7 ~ 6/9 | 프로젝트 발표영상 제작 및 
