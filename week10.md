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
