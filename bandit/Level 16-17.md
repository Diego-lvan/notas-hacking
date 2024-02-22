## Objetivo
The credentials for the next level can be retrieved by submitting the password of the current level to **a port on localhost in the range 31000 to 32000**. First find out which of these ports have a server listening on them. Then find out which of those speak SSL and which don’t. There is only 1 server that will give the next credentials, the others will simply send back to you whatever you send to it.
## Datos de acceso
JQttfApK4SeyHwDlI9SXGR50qclOAil1
bandit16
## Solución
```
	bandit16@bandit:~$ openssl s_client  localhost:31790
CONNECTED(00000003)
Can't use SSL_get_servername
depth=0 CN = localhost
verify error:num=18:self-signed certificate
verify return:1
depth=0 CN = localhost
verify error:num=10:certificate has expired
notAfter=Feb 22 18:04:08 2024 GMT
verify return:1
depth=0 CN = localhost
notAfter=Feb 22 18:04:08 2024 GMT
verify return:1
---
Certificate chain
 0 s:CN = localhost
   i:CN = localhost
   a:PKEY: rsaEncryption, 2048 (bit); sigalg: RSA-SHA1
   v:NotBefore: Feb 22 18:03:08 2024 GMT; NotAfter: Feb 22 18:04:08 2024 GMT
---
Server certificate
-----BEGIN CERTIFICATE-----
MIIDCzCCAfOgAwIBAgIEWdQAXzANBgkqhkiG9w0BAQUFADAUMRIwEAYDVQQDDAls
b2NhbGhvc3QwHhcNMjQwMjIyMTgwMzA4WhcNMjQwMjIyMTgwNDA4WjAUMRIwEAYD
VQQDDAlsb2NhbGhvc3QwggEiMA0GCSqGSIb3DQEBAQUAA4IBDwAwggEKAoIBAQC0
EWB28TWVpVUtrYSaYvmbjtrgpiTuEqg01/SReTOErvDgCyz8mhJ06BhcWK0RDiNz
E1BeQ1s7bo4V8knTeqgTd3cA9XIKO8BgqmGwYiPJyBVDMO+9S4dojnuJGViyhoM7
e0kKwdp7+uEER22koJg+ZqyI/dSSmvaDqMAU+D6FKxcxKjF8vTQzn0CLsYSXPHxT
mhshEAC8jWhYggcUxG0L1qMJnh/NL18e0jwBeCrE2PwsRuh1Qc6vl4Fd/mUByDJb
KSjsR3zDoegCWzh5lTAbnt5eaT47PBNA4foRLypdCG1tG+Cbgk6d0BGtluAJz9D8
5vEfrVpm38OelPOo0vBJAgMBAAGjZTBjMBQGA1UdEQQNMAuCCWxvY2FsaG9zdDBL
BglghkgBhvhCAQ0EPhY8QXV0b21hdGljYWxseSBnZW5lcmF0ZWQgYnkgTmNhdC4g
U2VlIGh0dHBzOi8vbm1hcC5vcmcvbmNhdC8uMA0GCSqGSIb3DQEBBQUAA4IBAQAl
z9TnfQ4cqpUeKMFRzhzuHEvuglEdfmmWmhpQ+NnpcI686OZDshzpHFRVUQjwMulr
XuhDoohLwnd+AOB4BqYWWYoF2z1mo3rsxZxxCoI7y8SP331O46Aqc4SyKMEfYBXq
mCaK5VQebSZotRPqI6jS2W7/+UmJXXKG4pEKI5pBA5tTnvNSbh6Yk87cFlAitTcN
36V1lq8S7tj2BZSfcC+nyoqwPPeLTb5beQTmKG0/JFDnYeHCbVQALq5AhXXH5G67
ytpppb4itSOMr9bfv+Awx6PPLbOJ/gxF1c1HkXX5/Pjbdy2W4sCykvXAJBir2BFe
ixo6bdA2sW0cz3uzk5x7

```
## Notas adicionales
nmap solo revisa los primeros 100 puertos mas utilizados, se puede especificar de la siguiente manera  ```nmap localhost  -p 31000-32000```
```
ssh -i llave bandit17@bandit.labs.overthewire.org -p 2220
```

## Referencias
