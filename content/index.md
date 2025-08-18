# Imepay Developer Documentation

## Last Updated 
September 20, 2021

## Introduction

IME Digital Solution Ltd. is a subsidiary of IME Group established under the payment and
settlement by laws 2072, with an aim to provide digital financial services to customers in
partnerships with banks/FIs as well as telecom operators and aggregators, deployed through self-
service as well as agent-based delivery channel.

IME Digital intends to introduce mobile money service, with name IME pay, under its digital
financial services initiative and offer a wide range of payment services to remittance customers
existent with money transfer associate company IME Ltd. and also cater to the vast majority of
unbanked and under-banked customers of Nepal. IME pay can be accessed via mobile and can be
serviced through any of the 20000 plus strong agent network of IME and beyond.

## Client Integration
This document describes the process for successfully integrating IME pay into your transaction
process, explaining how to facilitate communication between your mobile app and the IME pay.

Payment via IME Pay SDK completes in merely 3 steps:

1. Customer selects IME Pay as the payment method in merchant’s app.
2. Customer Enters wallet number and PIN.
3. Customer completes the transaction.

Note: this document helps to integrate IME Pay SDK to your native mobile app (iOS & Android)

**Prerequisites**

Merchants should create below api URL in order to integrate their mobile app with IME Pay

1. **Recording Service**:
Merchants accepting payments directly from mobile app are special merchant and thus,
must create a transaction recording api and provide the URL as parameter while calling
the method __performpayment__ in step 2. The API request response format is given in Step 4.
2. **Delivery Service**:
Merchant needs to create a delivery service webhook api, which accepts 5 parameters
that will inform the merchant system whether the payment is successful in IME pay or
not. And the details should be updated on the table. The API request response format is
given in Step 5





