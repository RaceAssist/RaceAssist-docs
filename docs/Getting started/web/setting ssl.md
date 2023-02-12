# Setting SSL

## How to create keystore.jks

```
sudo apt update
sudo apt install -y certbot
```

```
certbot certonly --standalone -d domain.com
```

```
cd /etc/letsencrypt/live/domain.com
```

```
openssl pkcs12 -export -in cert.pem -inkey privkey.pem -certfile chain.pem -out pkcs12.pfx -passout pass:<password> -name <keyAlias>
```

```
keytool -importkeystore -srckeystore pkcs12.pfx -srcstoretype PKCS12 -srcstorepass <password> -destkeystore keystore.jks -deststoretype JKS -deststorepass <password> -alias <keyAlias>
```

```
keytool -importkeystore -srckeystore keystore.jks -destkeystore keystore.jks -deststoretype pkcs12 -alias <keyAlias>
```