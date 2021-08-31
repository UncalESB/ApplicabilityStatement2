# How To Provide Uncal AS2 Cerificate
1. Create keypair using : `keytool -genkey -alias uncal-sender -keyalg RSA -keystore sender-keystore.jks`
2. Extract Public Key from `sender-keystore.jks` using : `keytool -export -alias uncal-sender -keystore sender-keystore.jks -file sender-trust.crt`
