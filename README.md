# Backend-Engineering

![OSI](https://user-images.githubusercontent.com/36560845/108817405-12004b80-75e2-11eb-9479-1e836c25f372.png)
## What is SSL
   - Secure Sockets Layer (SSL) is the standard security technology for establishing an encrypted link between a web server and a browser. The link ensures that all data passed between the web server and browsers remain private and integral. 
## How SSL certificate works:
When we type https://www.google.com in our browser and type ENTER , the following things happen
- Step 1: The browser requests secure pages from google server.
- Step 2: The google server sends its public key with its SSL certificate which is digitally signed by a third party or we call Certificate Authority (CA).
- Step 3: Once the browser gets the certificate, it'll check the issuer's digital signature to make sure the certificate is valid. A digital signature is created by a CA's private key and browsers like chrome or firefox is previously installed with many major CA's public keys, thus the signature is valid. Once the certificate's signature is verified, the digital certificate can be trusted. Now, a lock icon appears in the address bar. This lock icon indicates that the web server's public key really belongs to the web servers,not someone else. Verification is done, now its time to exchange a secret.
- Step 4: The browser creates one symmetric key or a shared secret. It keeps one and gives a copy to the web server. But the browser doesn't want to share the secret in plain text. Therefore, it uses the web server's public key to encrypt the secret and sends it to the web server.
- Step 5: When the web server gets the encrypted symmetric key, It uses its private key to decrypt it. Now the web server gets the browsers shared key. From now on, all traffic between the client and the web server will be encrypted and decrypted with the same key
