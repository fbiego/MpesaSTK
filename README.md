# MpesaSTK
An Arduino Library implementing MPESA Daraja on microcontrollers

[![arduino-library-badge](https://www.ardu-badge.com/badge/MpesaSTK.svg?)](https://www.arduinolibraries.info/libraries/mpesa-stk)

## Usage

### Initialize

```
//MpesaSTK mpesa(consumer_key, consumer_secret, pass_key);	//defaults to SANDBOX environment
MpesaSTK mpesa(consumer_key, consumer_secret, pass_key, SANDBOX);	//environment can be SANDBOX(default) or PRODUCTION
```

### Details
```
//TEST_CODE = 174379 
mpesa.begin(TEST_CODE, PAYBILL, "http://mycallbackurl.com/checkout.php"); //business code, type(PAYBILL or BUY_GOODS), callback url
```

### StkPush
```
mpesa.pay("2547XXXX__", 20, "Arduino", "Test");		//phone number, amount, reference, description
//String result = mpesa.pay("2547XXXX__", 20, "Arduino", "Test");	//get the result (json string)
```
