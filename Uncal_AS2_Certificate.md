# How To Provide Uncal AS2 Cerificate
1. Create keypair using : `keytool -genkey -alias uncal-sender -keyalg RSA -keystore sender-keystore.jks`
2. Extract Public Key from `sender-keystore.jks` using : `keytool -export -alias uncal-sender -keystore sender-keystore.jks -file sender-trust.crt`
3. import partner public key into `sender-keystore.jks` using : `keytool -import -alias uncal-receiver-public -keystore sender-keystore.jks -file receiver-trust.crt`
4. `sender-keystore.jks` now containt partner public key and can use on Uncal AS2 protocol
