Pulled from 'luomao2000@tom.com's APKEditor;

key.x509.pem
------------
```
    new-instance v0, Ljava/io/ByteArrayInputStream;

    const-string v1, "MIIBvzCCASigAwIBAgIESkrVyzANBgkqhkiG9w0BAQUFADAkMSIwIAYKCZImiZPyLGQBAQwSbHVvbWFvMjAwMEB0b20uY29tMB4XDTA5MDcwMTAzMTkzOVoXDTM5MDcwMTAzMTkzOVowJDEiMCAGCgmSJomT8ixkAQEMEmx1b21hbzIwMDBAdG9tLmNvbTCBnzANBgkqhkiG9w0BAQEFAAOBjQAwgYkCgYEArI6CCPCB7w+XA6dW8Y2QjG6pCgL+29zE1Fz6Tn8ig389pSlfd+ZthRktfcpwsZZ2762Mk8oOqYzFl2faU7ifKlOPGOzhaPd7Hm1Bzh8RMX55QDGodDJ14cR0pmetzuOyloYtfhAW+CzbX+ldmNwGq4zZJ9j+guq7OP//pTwUkJcCAwEAATANBgkqhkiG9w0BAQUFAAOBgQCBj0xSgoK8elQ8QTVRlwZ7Arlt6ooOfVh3kydawmQLlXf9WnTd8f6cn5bJ3v/FbUbcpokY1FqXjcHiZzlvRwzaW54WX2cZC9NluI/Nvl4U9q36XDseFDG4twB96PsZz3c0iUtD1V4fL/0fFBMsSpZ9u7rnapJhUDYg7yBkhTHYog=="

    invoke-static {v1}, Lcn/luomao/a/i;->a(Ljava/lang/String;)[B

    move-result-object v1

    invoke-direct {v0, v1}, Ljava/io/ByteArrayInputStream;-><init>([B)V

    const-string v1, "X.509"

    invoke-static {v1}, Ljava/security/cert/CertificateFactory;->getInstance(Ljava/lang/String;)Ljava/security/cert/CertificateFactory;

    move-result-object v1

    invoke-virtual {v1, v0}, Ljava/security/cert/CertificateFactory;->generateCertificate(Ljava/io/InputStream;)Ljava/security/cert/Certificate;

    move-result-object v0

    check-cast v0, Ljava/security/cert/X509Certificate;

    iput-object v0, p0, Lcn/luomao/b/l;->a:Ljava/security/cert/X509Certificate;
```

1. Copy the const-string
2. `pbpaste | base64 -D > key.x509.pem`

key.pk8
-------
```
    const-string v0, "MIICeAIBADANBgkqhkiG9w0BAQEFAASCAmIwggJeAgEAAoGBAKyOggjwge8PlwOnVvGNkIxuqQoC/tvcxNRc+k5/IoN/PaUpX3fmbYUZLX3KcLGWdu+tjJPKDqmMxZdn2lO4nypTjxjs4Wj3ex5tQc4fETF+eUAxqHQydeHEdKZnrc7jspaGLX4QFvgs21/pXZjcBquM2SfY/oLquzj//6U8FJCXAgMBAAECgYEAqsAd9uCfgsNniSsHAuI13nEGfqy2KzRL5WTYH+L4cSzxAEVvfgMb7vAaLvarC2A78zJGAFyao7Z0ND2FMwFnJWak1lxhVl/WstJ8UOxrd7aY3XkihC8Tm+Gos3MiIyu/vr36fPfgVJpcaS7Vx9lpo1KRwFmQZpNJrKoXRFvBlpECQQDlIhd32s+oNmc3eDHMeswovvsX6663++bov/VzZbuZjSRBSSdMqJmYxqTHg+Km6Bj6txD7TdXws+8rpIXoMpH/AkEAwMonsyMYz0Ea41HOV7GrLYwtsx80jBRJy6gqVDgyf8UDv3ADjmw7YTSV0sYoMvFClunOWFMRXPO8j5Yt5ttRaQJBAJhvpc1G9P+jsedlPzwaNdiltcakNQiRvXz6uACdncD59TS5xjtpr0XEYbuaMh94KaYiRFnr3njUPDl8qtlfS2ECQQC7I4Bl4yuyAwCWqFIjzdLb47Z4qVHYp9j6V8K+/c4HOLbqnVDWbzk0olbMwo1C5e49j7c9BWVVVUM0HhNwhHQBAkBBbW+6LoNaFCTvE0zuUitwUZO67RtwnyBnHR7iP3m3Tx09E/fUU0WHkhqu5gKjtc8X9iUj85kfQ7PH7bTB0ZH6"

    invoke-static {v0}, Lcn/luomao/a/i;->a(Ljava/lang/String;)[B

    move-result-object v0

    new-instance v1, Ljava/security/spec/PKCS8EncodedKeySpec;

    invoke-direct {v1, v0}, Ljava/security/spec/PKCS8EncodedKeySpec;-><init>([B)V
```

1. Copy the const-string
2. `pbpaste | base64 -D > key.pk8`