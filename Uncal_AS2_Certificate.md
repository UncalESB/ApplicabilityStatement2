# How To Provide Uncal AS2 Cerificate
1. Create keypair using : `keytool -genkey -alias uncal-sender -keyalg RSA -keystore sender-keystore.jks`
2. Extract Public Key from `sender-keystore.jks` using : `keytool -export -alias uncal-sender -keystore sender-keystore.jks -file sender-trust.crt` this public key is share to partner.
3. import partner public key into `sender-keystore.jks` using : `keytool -import -alias uncal-receiver-public -keystore sender-keystore.jks -file receiver-trust.crt`
4. `sender-keystore.jks` now containt partner public key and can use on Uncal AS2 protocol
5. Deploy `sender-keystore.jks` into Uncal AS2 protocol through Uncal Admin Page
