# How To Provide Uncal AS2 Certificate
1. Create keypair using : `keytool -genkey -alias uncal-esb -keyalg RSA -keystore uncal-keystore.jks`
2. Extract Public Key from `uncal-keystore.jks` using : `keytool -export -alias uncal-esb -keystore uncal-keystore.jks -file uncal-trust.crt` this public key is share to partner.
