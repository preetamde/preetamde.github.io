# x509 Certificates and Keys

Remember the following data is inserted by the CA into Certificate

1. Validity 
2. Subject
3. Issuer
4. Extensions
5. Versions

All this information is taken by CA and signed using Private Key of CA. Now, this becomes a signature which proves above data is valid.

When you see the following data. It is actually base64 encode

```bash
-----BEGIN CERTIFICATE-----
MIIGuDCCBaCgAwIBAgIQAQ5qgPxGrwbE1C+EdGDt9DANBgkqhkiG9w0BAQsFADBP
MQswCQYDVQQGEwJVUzEVMBMGA1UEChMMRGlnaUNlcnQgSW5jMSkwJwYDVQQDEyBE
aWdpQ2VydCBUTFMgUlNBIFNIQTI1NiAyMDIwIENBMTAeFw0yMjAyMTcwMDAwMDBa
Fw0yMjA4MTYyMzU5NTlaMGcxCzAJBgNVBAYTAlVTMRMwEQYDVQQIEwpDQUxJRk9S
TklBMRYwFAYDVQQHEw1TQU4gRlJBTkNJU0NPMRQwEgYDVQQKEwtSZWRkaXQgSW5j
LjEVMBMGA1UEAwwMKi5yZWRkaXQuY29tMIIBIjANBgkqhkiG9w0BAQEFAAOCAQ8A
MIIBCgKCAQEAz+maVKOkGuIpLUWBcrOoi0zOK7ui1z2eaWzzMtForAMdGnBV+IZa
QtyQ5++Gfv1TbOrAOKUntMp6luNeClruZSCzltfkOpk9eHJ9XWEUPrpFFCLbBVu9
1sl0EYvdWsplUlEgilO1zdDXr0UiyU0ptz14arWfA79ESEjl3EMIcCgfAumn5d9u
OQEkbOWAogF0Ed53rsoVVQoW+HVFVqdUlQ0boiQBdec9lKKDB8DbAEfdCC45zVjG
zA8Hhw4fmx1l4AlDqP2tLE2qNm2GhXjctrmexVjFG2t4nyihXllf92wvsEEGRZ8X
9pxVJTd/tfteIXPbe+u5DIE1ApPYcpfCBwIDAQABo4IDdjCCA3IwHwYDVR0jBBgw
FoAUt2ui6qiqhIx56rTaD5iyxZV2ufQwHQYDVR0OBBYEFHHgUNHngFL7IxRlnUOn
jTGqVmkmMCMGA1UdEQQcMBqCDCoucmVkZGl0LmNvbYIKcmVkZGl0LmNvbTAOBgNV
HQ8BAf8EBAMCBaAwHQYDVR0lBBYwFAYIKwYBBQUHAwEGCCsGAQUFBwMCMIGPBgNV
HR8EgYcwgYQwQKA+oDyGOmh0dHA6Ly9jcmwzLmRpZ2ljZXJ0LmNvbS9EaWdpQ2Vy
dFRMU1JTQVNIQTI1NjIwMjBDQTEtNC5jcmwwQKA+oDyGOmh0dHA6Ly9jcmw0LmRp
Z2ljZXJ0LmNvbS9EaWdpQ2VydFRMU1JTQVNIQTI1NjIwMjBDQTEtNC5jcmwwPgYD
VR0gBDcwNTAzBgZngQwBAgIwKTAnBggrBgEFBQcCARYbaHR0cDovL3d3dy5kaWdp
Y2VydC5jb20vQ1BTMH8GCCsGAQUFBwEBBHMwcTAkBggrBgEFBQcwAYYYaHR0cDov
L29jc3AuZGlnaWNlcnQuY29tMEkGCCsGAQUFBzAChj1odHRwOi8vY2FjZXJ0cy5k
aWdpY2VydC5jb20vRGlnaUNlcnRUTFNSU0FTSEEyNTYyMDIwQ0ExLTEuY3J0MAkG
A1UdEwQCMAAwggF8BgorBgEEAdZ5AgQCBIIBbASCAWgBZgB1ACl5vvCeOTkh8FZz
n2Old+W+V32cYAr4+U1dJlwlXceEAAABfwT+xw8AAAQDAEYwRAIgD3g+t2djijjQ
LkJ/gViH1xdXsIDFcboKF5ZaR7NAhQMCIAKLl0jdDpHNz6LmdnVmm6V3e+poMt9v
ZosMBBuMbn+TAHYAQcjKsd8iRkoQxqE6CUKHXk4xixsD6+tLx2jwkGKWBvYAAAF/
BP7G7AAABAMARzBFAiEA5kbrW2wUoFoevlbavsS/TRhxth+wcfUBWGSdlnIw24YC
IAU/+LllzFfvo7WzvdieZDhx4IPXsdYwIbRyIGZTmqxzAHUA36Veq2iCTx9sre64
X04+WurNohKkal6OOxLAIERcKnMAAAF/BP7HIAAABAMARjBEAiA20sYE2dhU2bRU
cq91JlEgW5QYiBLIqQYLrtDjd94toAIgP787sG2IkEwqQ9n+NLibq1fHN+Neg3MY
rRSMJSPW42owDQYJKoZIhvcNAQELBQADggEBALxVWirhjYiCYuzYYGdJPR3lEnDt
bCj2qzkTb+19sFwEBRyP8SKu6fyePOBVdZadu+zk/7ar/6O9cYQ4xl3Zz1IjFq2S
rKVwr9un3CMRYP9lUy6Jgt9j0Y1QukFMxu4rv61rbuOoAgMzkcOOIj7rxJCCbrR1
YV8+Y8fgp85SKxi+wO77DVLxdDpJd2ZwzvH7iknuK2IChlNKQPuaMuzzDejAlEW5
XHXNNtAScl8eXWo2vjG9a1zrc7mU26yxFm/5a386OokM1zSjdSV80fWkJ7T9VUuu
2VEJ9RLvpaZCVKO7n9gxMIGqadOUA7bJmZ7zswAQG2xjXVMXqwLeNwOUVno=
-----END CERTIFICATE-----
```

Let take the above data and put in a file named redditcert

The importance of flag `text`. I have used this `-text`flag several times but never understood what it means. It means "please give me the information in human readable format". But if you run below command, the output would be same as above.

```bash
openssl x509 -in redditcert
```

Here you will get same information as was in redditcert. But to make it human readable, you have to use `-text` flag. So the command would look like

```bash
openssl x509 -in redditcert -text -noout
```

You might ask, what is this `-noout` flag. Well this flag tells, please do not send the output in base64 format. And `-text` , we are telling to send the output in human readable format.

### What is inside CSR?

CSR includes the following three parts

1. Certificate Request Info
2. Signature Algorithm
3. Signature

#### Note:

It is server who creates CSR. That means, key is created by the server.

### File Formats

when file is streams on wire it is 1 and 0. So when you transfer certificates on wire it use DER.
DER stands for Distinguished Encoding Rules

#### PEM

Privacy Enhanced Mail. It is base64 file format representing DER format.
Every 6 bits is translated into a character.
PEM is very popular format as it is easy to copy the contents of file between different computers.
One PEM file can contain more than one certificate e.g. public and private key.
It is basically pem formatted file. This does not mean, it will have `pem` extension

#### PFX or PKCS#12

1. PFX     = Public Information Exchange (originally developed by microsoft in 1996)
2. PKCS    = Public Key Cryptography Standard #12

Since file names are of 3 characters, it is used as `.pfx`. PFX as a file format is no longer used.
It can contain, one certificate and matching key.  Also potentially a certificate chain.
These are binary file (human non-readable) and contain following three file extensions

1. `.pfx`
2. `.p12`
3. `.pkcs12`

#### pkcs7

1. popular. It contains certificate. No keys. but key is part of certificate. It can also contain certificate chain
2. file starts with `-----BEGIN pkcs7-----`
3. Typically not used for SSL and TLS
4. Was used for SMIME
5. File extensions used are 
   1. `.p7c`
   2. `.p7b`
   3. `.pkcs7`

### Converting PEM formatted files

Let's do some converting from one file format to another. Few commands we should try.

#### Converting from PEM to PFX

```bash
# in the below command, remember -export and -inkey
openssl pkcs12 -in nameofthefileinPEMformat -inkey nameoftheprivatekey -export -out nameofthepfx

# check the PFX file. Remember -nodes. Here 'no' means I do not want DES encryption.

openssl pkcs12 -in namefilepfxfile -nodes -info

```

In above command you will need to enter password but it is optional. As mentioned above, `pfx/pkcs12` contains both certificate and matching key, while exporting it, we need to specific both key and cert file.

#### Convert PEM to DER

Always remember `-outform` is used only in this conversion. The example of the command is

```bash
# convert from PEM to DER. remember -outform
openssl x509 -in filename.crt -out filename.der -outform DER

# check this DER FILE

openssl x509 -in filename.der -inform DER -noout -text

#example
openssl x509 -in sam.com.DER.clcert -inform DER -noout -text

```

*Note: You cannot convert a DER file into PFX, it should be PEM first and then PFX.* That is `DER -> PEM -> PFX`

#### Converting PKCS

This is quite interesting about `pkcs12`. What you learn in the theory, you could apply here.
so, first command is to dump everything. In short nothing to mentioned in the argument

```bash
# output everything
openssl pkcs12 -in sam.com.PFX -out sam.com.all

#inspect if there everything in call
cat sam.com.all
Bag Attributes
    localKeyID: 10 E7 30 27 86 6B 79 2A 7D 73 D7 68 D4 E8 9B 89 70 11 43 93 
subject=/C=US/ST=Middle Earth/L=The Shire/O=Hobbits/CN=sam.com
issuer=/C=US/ST=Middle Earth/L=Rivendell/O=White Council/OU=Grey/CN=Gandalf the CA
-----BEGIN CERTIFICATE-----
MIIE0TCCArmgAwIBAgIUWnRxP6npEv7jDcayOF1BBWkukv0wDQYJKoZIhvcNAQEL
-----END CERTIFICATE-------
Bag Attributes: <No Attributes>
subject=/C=US/ST=Middle Earth/L=Rivendell/O=White Council/OU=Grey/CN=Gandalf the CA
issuer=/C=US/ST=Middle Earth/L=Rivendell/O=White Council/OU=Grey/CN=Gandalf the CA
-----BEGIN CERTIFICATE-----
MIIF0TCCA7mgAwIBAgIUGFuj7Eypg3kBTbJ52euaYoSgq+4wDQYJKoZIhvcNAQEL
-----END CERTIFICATE-------
Bag Attributes
    localKeyID: 10 E7 30 27 86 6B 79 2A 7D 73 D7 68 D4 E8 9B 89 70 11 43 93 
Key Attributes: <No Attributes>
-----BEGIN PRIVATE KEY-----
MIIEvQIBADANBgkqhkiG9w0BAQEFAASCBKcwggSjAgEAAoIBAQCjOTGqCJ8jkMYH
-----END PRIVATE KEY------
```

In the above redacted output, there are multiple certificates

1. Private key
2. Two certificates (CA and Server certificate)
3. Issuer and subject details

##### Getting only certs out of pkcs12

As `pkcs12` contains many files, using right flags, we have possibility of extracting things we need.

```bash
# lets take the same PFX file and extract certificates. Worth to remember that we do not use -nodes 
# because we are simply exporting certs
openssl pkcs12 -in sam.com.PFX -out sam.com.certs -nokeys

# lets check the output

openssl x509 -in sam.com.certs -noout -text

Certificate:
    Data:
        Version: 3 (0x2)
        Serial Number:
            5a:74:71:3f:a9:e9:12:fe:e3:0d:c6:b2:38:5d:41:05:69:2e:92:fd
    Signature Algorithm: sha256WithRSAEncryption
        Issuer: C=US, ST=Middle Earth, L=Rivendell, O=White Council, OU=Grey, CN=Gandalf the CA
        Validity
            Not Before: Oct  6 01:18:14 2020 GMT
            Not After : Oct  6 01:18:14 2021 GMT
        Subject: C=US, ST=Middle Earth, L=The Shire, O=Hobbits, CN=sam.com
        Subject Public Key Info:
            Public Key Algorithm: rsaEncryption
                Public-Key: (2048 bit)
                Modulus:
                    00:a3:39:31:aa:08:9f:23:90:c6:07:10:ce:67:2b #redacted
                Exponent: 65537 (0x10001)
        X509v3 extensions:
            X509v3 Basic Constraints: 
                CA:FALSE
            X509v3 Subject Key Identifier: 
                9D:C2:C7:86:12:C3:4B:73:69:25:C1:D0:94:1D:AB:84:75:CD:FC:3D
            X509v3 Authority Key Identifier: 
                keyid:C0:CF:FD:E3:5F:44:01:D8:09:45:69:5E:37:C2:00:01:88:D7:F4:48
            X509v3 Key Usage: 
                Digital Signature, Key Encipherment
            X509v3 Extended Key Usage: 
                TLS Web Server Authentication
    Signature Algorithm: sha256WithRSAEncryption
         74:80:54:29:4c:ab:3d:4c:e3:6f:5f:90:9d:62:f1:1e:ef:a4: #redacted

# cat output of cat sam.com.certs 

cat sam.com.certs                          
Bag Attributes
    localKeyID: 10 E7 30 27 86 6B 79 2A 7D 73 D7 68 D4 E8 9B 89 70 11 43 93 
subject=/C=US/ST=Middle Earth/L=The Shire/O=Hobbits/CN=sam.com
issuer=/C=US/ST=Middle Earth/L=Rivendell/O=White Council/OU=Grey/CN=Gandalf the CA
-----BEGIN CERTIFICATE-----
MIIE0TCCArmgAwIBAgIUWnRxP6npEv7jDcayOF1BBWkukv0wDQYJKoZIhvcNAQEL #redacted
-----END CERTIFICATE-----
Bag Attributes: <No Attributes>
subject=/C=US/ST=Middle Earth/L=Rivendell/O=White Council/OU=Grey/CN=Gandalf the CA
issuer=/C=US/ST=Middle Earth/L=Rivendell/O=White Council/OU=Grey/CN=Gandalf the CA
-----BEGIN CERTIFICATE-----
MIIF0TCCA7mgAwIBAgIUGFuj7Eypg3kBTbJ52euaYoSgq+4wDQYJKoZIhvcNAQEL #redacted
-----END CERTIFICATE-----

```

In above, there are two certificates. CA and Server certificate

##### Getting only CA certificates

```bash
output only ca certs using -cacerts flag
openssl pkcs12 -in sam.com.PFX -out sam.com.cacerts -nokeys -cacerts

# check if that is CA, using basicConstraints ext

openssl x509 -in /tmp/sam.com.cacerts -noout -ext basicConstraints
X509v3 Basic Constraints: critical
    CA:TRUE

```

##### Additional commands

```bash
# outputs only keys. No Certs
openssl pkcs12 -in sam.com.PFX -out sam.com.key -nodes -nocerts

# output only client certs

openssl pkcs12 -in sam.com.PFX -out sam.com.certs -nokeys -clcert

# now combining above, i.e. private and clcert

openssl pkcs12 -in sam.com.PFX -out sam.com.cert.key -nodes -clcert

# From the file above, you can use both rsa and x509 flat to extract the respective outputs

# to extract private key
openssl rsa -in sam.com.cert.key -noout -text

# to extract certificate
openssl x509 -in sam.com.cert.key -noout -text


```
