## WEEK 10
	

<황의혁>


<build.gradle 에 라이브러리 추가>

    implementation 'com.android.billingclient:billing:3.0.1'

    implementation 'com.android.billingclient:billing-ktx:3.0.1'

    implementation 'com.google.android.gms:play-services-base:17.4.0'1'


<Manifest.xml 에 permission 추가>

    <uses-permission android:name="com.android.vending.BILLING" />

<activity쪽에 추가>

    PurchasesUpdatedListener,
   
    PurchaseHistoryResponseListener {

    private lateinit var binding: ActivityMainBinding
   
    private lateinit var billingClient: BillingClient
   
    private val purchasableList = ArrayList<String>()
 	
    override fun onCreate(savedInstanceState: Bundle?) {
        super.onCreate(savedInstanceState)
		
        binding = DataBindingUtil.setContentView(this, R.layout.activity_main)
		
        initBillingClient()
    }

<Billing Client를 초기화 해주고>

    private fun initBillingClient() {
	
    billingClient = BillingClient.newBuilder(this).enablePendingPurchases().setListener(this).build()
	
    billingClient.startConnection(object : BillingClientStateListener {
	
    override fun onBillingSetupFinished(billingResult: BillingResult) {
	
    if (billingResult.responseCode == BillingClient.BillingResponseCode.OK) {
  

<나머지 코드는 구글플레이에 아직 개발자로 등록되지 않아
  콘솔에 지정할 id와 일치 하지 않습니다.
  개발자 승인을 받고 난 후 코드 수정하겠습니다.>
  
  
     private fun setPurchasableList() {
  
    // Google PlayConsole 의 상품Id 와 동일하게 적어준다
	
    purchasableList.add("always_item") // 중복해서 무제한으로 살 수 있는 아이템
	
    purchasableList.add("one_item") // 1번만 살 수 있는 아이템
}

<한창훈>
회원가입과 내 정보를 입력했으면 이를 볼 수 있어야 하고 정보 수정, 비밀번호 재설정, 회원 탈퇴도 해야함으로 이번주부터 이 기능들을 구현하고 있다. 

먼저 회원정보 수정기능을 하기 위해 DB에 저장된 데이터를 가져와야 한다. 그러기 위해선 현재 로그인 되어있는 유저에 정보를 가져와야함으로 아래 코드를 작성한다.
FirebaseUser user = FirebaseAuth.getInstance().getCurrentUser();
database = FirebaseDatabase.getInstance();

이제 유저에 저장되어있는 이름, 주소, 생년월일, 전화번호 등을 가져온다.
DatabaseReference userRef = database.getReference("users").child(user.getUid());

userRef.addListenerForSingleValueEvent(new ValueEventListener() {
    @Override
    public void onDataChange(@NonNull DataSnapshot snapshot) {
        String name = snapshot.child("name").getValue(String.class);
        String address = snapshot.child("address").getValue(String.class);
        String phoneNumber = snapshot.child("phoneNumber").getValue(String.class);
        String birthDay = snapshot.child("birthDay").getValue(String.class);

        nameCon.setText(name);
        addressCon.setText(address);
        phoneCon.setText(phoneNumber);
        birthCon.setText(birthDay);
    }

    @Override
    public void onCancelled(@NonNull DatabaseError error) {    }
});

하지만 데이터를 가져오는 과정에서 오류가 생겨서 해결하는 데 많은 시간을 썼다. 
이 후 해야 할 일은 수정한 정보를 EditText에 적고 이 값으로 해당 DB에 값을 바꿀 것이고 탈퇴를 누르면 저장되어 있던 user에 정보를 완전히 삭제할 예정이다. 

<안세준>

<img src="https://user-images.githubusercontent.com/29851772/117683668-43ef7a00-b1ef-11eb-9bea-b611d98ff40c.PNG" width="250" height="500">

- 채팅방 구현 및 디자인

Navigation Bar를 사용하여 Fragment 화면 전환을 하는데 xml파일에서 디자인한 결과와 실제 핸드폰에서 보이는 화면이 다르고 백그라운드 이미지가 밀리는 현상이 발생했다.
해결법으로 백그라운드 이미지를 사용하지않고 이미지뷰를 화면에 맞게 넣어주는 방법을 택했는데 이미지뷰의 비율이 잘 맞지 않아 여러 방법을 시도해본 결과 해결하였다. 

채팅 기능 구현하는파트를 맡았는데 파이어베이스를 사용해야해서 코드를 찾아보았다. 관련한 코드가 있는데 오류가 많아 오류를 잡기위해 
공부중이다. 

채팅목록중 하나를 클릭하여 채팅방에 들어가는 기능은 구현했는데 확인하지 않은 메시지 중 마지막에 받은 메시지 혹은 내가 마지막에 보낸 메시지를 
채팅방 미리보기에 띄워줘야하는데 방법을 찾는중이다. 

<김홍진>

프래그먼트로 변경된 학과 게시판을 프래그먼트로 옮기고 게시글을 누르면 화면이 뜨고 댓글을 작성하면 데이터베이스에 들어가고 그 값을 받으면 화면에 띄워주게 했다.

<img width="40%" src="https://user-images.githubusercontent.com/29851704/117681234-db070280-b1ec-11eb-81bf-8652d693649d.gif"/>

<img width="40%" src="https://user-images.githubusercontent.com/29851704/117681237-dcd0c600-b1ec-11eb-9bab-f8fdc0bfa8e8.gif"/>

<데이터값 받아오기>
  replyRef.addValueEventListener(new ValueEventListener() {
            @Override
            public void onDataChange(@NonNull DataSnapshot snapshot) {
                replyList.clear();

                for(DataSnapshot snap : snapshot.getChildren()){

                    Map<String, Object> map = (Map<String, Object>) snap.getValue();
                    String content = String.valueOf(map.get("content"));
                    ReplyInfo replyInfo = new ReplyInfo(userName,content);

                    //ReplyInfo replyInfo = snap.getValue(ReplyInfo.class);

                    replyList.add(replyInfo);

                }

                replyAdapter.notifyDataSetChanged();
            }
	    문제점: 이 부분에서 데이터를 불러올때 다른 유저들이 쓴 댓글을이 불러와야 되는데 로그인한 유저가 쓴 댓글만 받아진다. 
	    
<정지원>	 

- 랜덤매칭 및 매칭을 위한 관심사 설정 페이지

<img src="https://user-images.githubusercontent.com/29966841/117688810-1953f000-b1f4-11eb-9de0-5255550197c2.png" width="250" height="500">

-> 랜덤매칭을 위한 사용자의 관심사 설정 페이지를 구현하였고, 화면 하단의 '관심사 설정' 버튼을 누르게 되면 랜덤매칭이 진행되도록 할 예정이다.

<img src="https://user-images.githubusercontent.com/29966841/117689113-6768f380-b1f4-11eb-90cc-f1a066b46c3c.png" width="600" height="400">

-> 랜덤매칭을 위한 코드들을 넣어주었고 오류도 모두 해결하였는데 어플리케이션을 실행하게되면 위의 사진과 같이 어플리케이션이 멈춰버리게 된다.
   MainActivity코드의 문제인 것 같아서 현재 해결중에 있다.


