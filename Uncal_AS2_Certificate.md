# How To Provide Uncal AS2 Certificate
1. Create keypair using : `keytool -genkey -alias uncal-esb -keyalg RSA -keystore uncal-keystore.jks`
2. Extract Public Key from `uncal-keystore.jks` using : `keytool -export -alias uncal-esb -keystore uncal-keystore.jks -file uncal-trust.crt` this public key is share to partner.
3. Import partner certificate into `uncal-keystore.jks` using `keytool -import -alias partner-certificate -keystore uncal-keystore.jks -file partner-trust.crt`

these keystore has provide in this repo for Uncal AS2 connector testing purpose.
`uncal-keystore.jks` already import partner certificate also vice versa, so the keystore is just deploy at Uncal Admin page and it will be appear in UIC AS2 Connector configuration
### properties of `uncal-keystore.jks`
key-pass : test1234\
store-pass : test1234\
uncal-alias : uncal-sender\
partner-alias : mule-public
### properties of `mule-keystore.jks`
key-pass : test1234\
store-pass : test1234\
mule-alias : mule-sender\
partner-alias : uncal-public
### gambarnyah kayak ginih yah
![alt text](https://github.com/UncalESB/NVR_Hikvision/blob/main/CFG_uncalAS2_dan_Partner.png)
