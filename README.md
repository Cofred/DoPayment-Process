# DoPayment-Process
DoPayment Process guide for API

This method is used to perform Transfer between Cofred Accounts

HTTP Method: POST

# Resource Url

https://cofred.com/secure/api/v1/doPayment

# Headers

See our Guide for how to setup Header https://github.com/cofred/Header-Authentication

# Authentication Headers Example

merchant_id: VF9CMTY3WURPZUpJdkNnVWJWRXE=   // Base64 Encoded

secret_code: I8AtLUljNqcdS4F76OVy2Zf1bJvGwsP95rE

terminal_id: YINCU

access_token: dUp4dEtybVg0Ump4MEFT  // Base64 Encoded

timestamp: 1505628722

# Request Parameters

Field	M/O	Length	Format	Description

Account Number	M	10	Numeric	Account Number to get Name

Amount	M		Numeric	Transaction Amount

Reference	M		Alpha Numeric	Merchant Reference ID

Benificiery Last Name	O			Last name of Benificiery

Benificiery Email	O			Email Address of Benificiery

Benificiery Phone	O			Phone Number of Benificiery

Payment Channel	M			
				
# DoPayment Response

A HTTP response code 200 is sent back for a success

# Response Parameters

Field	Description

responseCode	Response Code

TransactionReference	Unique Transaction reference generated by Cofred

TransactionDate	Date and Time of Transaction

responseMessage	Response Message which will return Transaction success message

# Sample Response

200

{
  "responseCode":"200",
  "TransactionReference":62746444,
  "TransactionDate":"2017-09-17 18:35:06",
  "responseMessage":"Transaction successfull!"
}

# Communication

Requests will be sent over the REST protocol using POST Method.
