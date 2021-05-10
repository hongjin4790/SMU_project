<week10>
	

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


