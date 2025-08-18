Receive payment from your customer through IME pay.

Overview
--------

1. Introduction
2. SDK Feature
3. SDK Initialization
   * Authenticate Merchant
   * Get Transaction Token
   * Perform Payment
   * Validate Payment
4. Response Codes
5. Sample Code
6. Releases

Introduction
------------

The IME Pay Payment SDK for Android gives access to merchants to receive payment from IME Pay customers through their native android application.

SDK Features
------------
IME pay Android Merchant Payment SDK enables merchants to receive payments from IME pay customes through their native application. The application performs the payment and verifies the transaction status.

SDK Initialization 
------------------

1. In your project, open your_app > Gradle Scripts > build.gradle (Module: app) and add the following implementation statement  to the dependencies{} section to depend on the latest version of the IMEPay Merchant SDK: 
  ```java
  implementation 'com.swifttechnology.imepaysdk:payment-service:4.0.1'
  ```
2. In your activity create an instance for IMEPayment.
  ```java
    IMEPayment imePayment = new IMEPayment(activity.this, ENVIRONMENT.LIVE);
  ```
  
!> Note : Use `ENVIRONMENT.TEST` for test purposes.


Authenticate Merchant / Get Transaction Token
---------------------------------------------

The merchant is verified using the merchant code, merchant username, merchant password, module which will be provided by the IME pay Developer Support to applicable merchants. 

Perform Payment
---------------

This SDK enables merchants to receive payments through IME pay, using the instance of IMEPayment call the method performpaymentV1().

```java
IMEPayment imePayment = new IMEPayment(activity.this, ENVIRONMENT.LIVE);
imePayment.performPaymentV1(
       merchantCode.getText().toString(),
       merchantName.getText().toString(),
       merchantUrl.getText().toString(), deliveryUrl.getText().toString(),
       amount.getText().toString(),
       refId.getText().toString(),
       module.getText().toString(),
       user.getText().toString(),
       password.getText().toString(),
       new IMEPaymentCallback() {
@Override
public void onSuccess(int responseCode, String transactionId, String msisdn,
String amount, String refId) {
// Response Code 100 : Transaction successful.
// Response Code 101 : Transaction failed.
// transactionId : Unique ID generated from IME pay system
// amount: Amount paid by customer
// refId : Reference Value
}
//Override
//public void onTransactionCancelled(String refID){
// Your code to handle , if transaction cancelled by user //}
});


```

Validate Payment
----------------
After performing payment the SDK will verify the payment. This feature is handled by the SDK itself. On the basis of the validate payment response the developer will get a response in IMEPaymentCallback(). There are two types of responses that a developer can get in IMEPaymentCallback 

* Response Code 100 : 
  Transaction was successfully executed and verified.

* Response Code 101 : 
  Transaction request was successfully sent, but could not get verified. The customer executing the payment will get an SMS for the confirmation.

IMPORTANT NOTE : Merchant Transaction Recording URL
---------------------------------------------------
Merchants accepting payments directly from mobile application should be a special merchant and thus, must create a transaction recording api and use the URL as a parameter while calling the method perform payment. Please get the request and response parameter details from IMEPAY Merchant Team.

Response Codes
--------------
These response codes mentioned below are handled by the SDK itself.

* 403 : Application unauthorized to use the service.
* 500 : Your request cannot be processed at the moment
* 401 : Application request cannot be processed at the moment

Sample Code
-----------

[ Click here for Sample Code ](https://github.com/imepay/imepaySDK_android/blob/master/SampleActivity.java)

Assets
------

[ Click here for IMEPAY Logo](https://raw.githubusercontent.com/imepay/imepaySDK_android/master/imepaylogo.svg)



Releases
-----------

1. v1.1
2. v1.2
3. v1.3
   * Fixed issue related to payment in live portal
4. v2.0
5. v2.1
   * Fixed issue with text color inside PIN edit text
6. v3.0.1
   * New Flow implemented with 2 factor user validation
   * Customer mobile number is prompted in the SDK itself


