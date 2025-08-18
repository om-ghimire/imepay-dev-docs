
## Woo Commerce WordPress



### IME pay Checkout Process Overview:

This document describes the process for successfully integrating IME pay into your transaction
process, explaining how to facilitate communication between your Woo commerce built website
and the IME pay, and how to setup the plugin.

IME Pay checkout process will be completed in 4 to 5 steps.


### Steps in IME pay Checkout:

### STEP 1

The first step involves process of installing up IME pay Woo Commerce Plugin. Merchant needs
to setup the plugin to their WordPress website. The process involved are:

1. Download the ZIP file provided by IMEPAY
2. Go to the plugin section in your WordPress admin dashboard
3. Click on Add New and upload the zip file of IMEPAY Woo Commerce plugin and
    upload it.
4. After Upload click on install now and activate the plugin.

### STEP 2

The Second step involves process of Setting up IME pay Woo Commerce Plugin.
Merchant needs to setup the plugin to their WordPress website. The process involved are

1. After installation is complete, go to Woo Commerce > Settings.
2. Go to Payments option where you can find IMEPAY among other payment gateways
3. Click on IMEPAY option and enter your test or live credentials accordingly provided
    by IMEPAY (Shown below).


Parameters:

1. Enable / Disable: To make the plugin working you need to make sure “Enable
    imepay payment” is ticked.
2. Title: Display name refers to the name that your users see at the time of payment.
    (Name could be your choice. E.g. IMEPAY or IMEPAY gateway).
3. Description: In the description field you can add any text you want that describes
    the payment gateway perfectly.
4. IME Username: API username is your merchant username provided by IMEPAY
    itself during registration.
5. Password Code: User Password is the password of your merchant username.
6. Merchant Code: Merchant code is the unique code provided to you to represent
    your business by IMEPAY during registration
7. Module Name: Module Name is provided by IMEPAY at the time of registration.
8. Invoice Prefix: You can add any prefix text or number that you want to give to the
    invoice number. (You can also leave the field blank).
9. Sand Box Mode: Sand Box mode enables you to test the API without spending any
    money for checking the API. If you enable the test mode, you should fill all above
    credentials (API Username, Merchant Code, User Password Key and Module
    Name) according to the test credentials provided by IMEPAY.

NOTE: Currency for processing: You need to select NPR if you have setup multiple
currency in your Woo commerce website

After all above setup you can create a demo product and begin testing. The expected output
is shown below of process involved in buying a product and choosing IME pay as payment
gateway.


### STEP 3

Merchant’s page is redirected to IME pay Web Checkout page. It initially validates the TokenId
against the MerchantCode, RefId, and Amount sent. In case of failure, error page is displayed. If
successful, customer wallet account input form is displayed. Customer verifies transaction
amount, and Merchant Name, if satisfied, enters wallet id and PIN (Personal Identification
Number) associated with IME pay and clicks “Proceed Pay” button.

Note:
If customer is not satisfied with the payment details, he/she can abort the operation by closing
the window or by clicking the Cancel Pay button. If Cancel pay button is pressed, customer will
be redirected to the invoice page of the order.


### STEP 4

If combination of entered mobile number and PIN is correct, customer will receive SMS in his/her
mobile containing OTP (One Time Password). Customer then must enter the OTP and press
Confirm Pay button to process the transaction.

Note:
If customer decides to cancel the transaction in this stage, he/she can abort the operation by
closing the window or by clicking the Cancel Pay button. If Cancel pay button is pressed,
customer will be redirected to the invoice page of the order.

### Download woo commerce: 
 [click here](/assets/IME%20Pay%20WooCommerce%20Plugin%20V1.1.zip ':ignore click to download woo commerce file')


## IME pay WHMCS Plugin


### IME pay Checkout Process Overview:

This document describes the process for successfully integrating IME pay into your transaction
process, explaining how to facilitate communication between your Woo commerce built website
and the IME pay, and how to setup the plugin.

```
IME Pay checkout process will be completed in 4 to 5 steps.
```

### Steps in IME pay Checkout:

### STEP 1

The first step involves process of installing up IME pay WHMCS Plugin. Merchant needs to
setup the plugin to their WHMCS website. The process involved are:
1) Download the ZIP file provided by IMEPAY
2) Simply extract at the root folder of your WHMCS installation. Following files should be
copied in following directories.

```
File Structure
```
```
modules /
| gateways /
| imegateway.php^1
| callback /
| imegateway.php 2
| imegateway /
| imelogo.png^3
```
```
1. Inside your WHMCS installation folder you find the modules folder and following by,
you get gateways folder.
2. You need to add imegateway.php^1 file from the extracted zip to that very same folder.
3. Secondly create an imegateway folder inside it and add imelogo.png^3 file.
4. Navigate to the callback folder inside gateways folder and upload the callback file named
imegateway.php^2 from the callback folder of provided zip.
```
```
[Numbers represents file from above file structure]
```

> Note:
For the Imepay payment gateway module to work, your website hosting server need to have
enable the 7979 TCP port and have whitelisted 202.1 6 6.194. 90 Further again if the plugin is
not working you need to contact IME Pay support team and ask them to whitelist your website
IP address.


### STEP 2

```
Login to admin area of your WHMCS installation and enable the gateway from Setup -
> Payments - > Payment Gateways (Refer to the image below)
```
1. Go to Payments option where you can find IMEPAY among other payment gateways
2. Click on IMEPAY option and enter your test or live credentials accordingly provided
    by IMEPAY (Shown below).


3. Once the gateway is enabled, the gateway parameters need to be configured.
    Navigate to manage existing Gateways (Refer to the image below)

```
Parameters:
```
1. Display Name: Display name refers to the name that your users see at the time of
    payment. (Name could be your choice. E.g. IMEPAY or IMEPAY gateway)
2. API Username: API username is your merchant username provided by IMEPAY itself
    during registration
3. Merchant Code: Merchant code is the unique code provided to you to represent your
    business by IMEPAY during registration
4. User Password Key: User Password is the password of your merchant username.
5. Module Name: Module Name is provided by IMEPAY at the time of registration.
6. Test Mode: Test mode enables you to test the API without spending any money for
    checking the API. If you enable the test mode, you should fill all above credentials (API
    Username, Merchant Code, User Password Key and Module Name) according to the test
    credentials provided by IMEPAY.
7. Convert for processing: You need to select NPR if you have setup multiple currency in
    your WHMCS panel.

(^)
Note:

1. Please make sure that the currency "NPR" is selected for the option "Convert to For
    Processing".
2. If you are using test mode, then the credentials should be filled accordingly.

```
After all above setup you can create a demo product and begin testing. The expected output is shown
below of process involved in buying a product and choosing IME pay as payment gateway.
```

### STEP 3

Merchant’s page is redirected to IME pay Web Checkout page. It initially validates the TokenId
against the MerchantCode, RefId, and Amount sent. In case of failure, error page is displayed. If
successful, customer wallet account input form is displayed. Customer verifies transaction
amount, and Merchant Name, if satisfied, enters wallet id and PIN (Personal Identification
Number) associated with IME pay and clicks “Proceed Pay” button.

Note:
If customer is not satisfied with the payment details, he/she can abort the operation by closing
the window or by clicking the Cancel Pay button. If Cancel pay button is pressed by the
customers, they will be redirected to the invoice page of the order section immediately.


### STEP 4

If combination of entered mobile number and PIN is correct, customer will receive SMS in his/her
mobile containing OTP (One Time Password). Customer then must enter the OTP and press
Confirm Pay button to process the transaction.

Note:
If customer decides to cancel the transaction in this stage, he/she can abort the operation by
closing the window or by clicking the Cancel Pay button. If Cancel pay button is pressed,
customer will be redirected to the invoice page of the order.

### Download WHMCS Plugin : 
 [click here](/assets/IME%20Pay-whmcs%20V1.0.zip ':ignore click to download whmcs file')

### Contacts

Rajesh Shrestha - Business Analyst
rajesh.shrestha@imeremit.com.np
Ph. 9801190734





