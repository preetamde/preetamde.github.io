# Module:01

## Chapter:02

SSL and TLS have same purpose. TLS is much higher version than SSL. SSL was developed by Netscape in 1994 and later was taken over by IETF. IETF (Internet Engineering Task Force) renamed SSL as TLS.
Basically, SSL is HTTP over SSL. That is literally HTML page is transferred with HTTP Protocol using SSL.
So, it is referred as HTTPS. HTTP is protocol.
When you browsing website, then between you and the website there are many ISP Routers responsible to display the website to you.
But without HTTPS, anyone can read or view this traffic. For reading blogs, won't make much difference. However, when you wish to enter you credentials, then this really bad idea from the security perspective as everything goes in plain text.

### HTTPS

Here comes
Here SSL/TLS is trying to solve three problems

1. Ability to securely connect to the website
2. Ability to secure connect to the corporate resources
3. Ability to hide your Public IP to browse the internet anonymously.

## Chapter:03

Interesting concepts. I'm surprised and moved how things are interconnected.

### CIA Principle

1. Confidentiality through Encryption
2. Integrity through Hashing
3. Authentication through PKI

## Chapter:04

### Anti-replay

Anti-replay is built into SSL/TLS. But what is anti-replay. When you send encrypted message across the wire, someone can pick this encrypted message and send it to the destination multiple times. This is kind DDoS attached. *I might be wrong*. Anti-replay is avoided using sequence number.

### Non-Repudiation

Here you simple cannot deny that you have not send this data or own this data. This is achieved in combination of Authentication (it is you, confirmed by providing credentials) and Integrity (no one change the data or tamper it, including yourself)

## Chapter:05 - Keyplayers

### Clients

Here clients are defined as devices (phone, Smart Toaster, IoT) which can *initiate* connection with Internet. So, it is not you and me. It is device which is capabale of initiation the connection. In this time and year, I would say this connection is normally a internet connection to some service somewhere.

### Servers

Servers are the one who *recieves* TLS Handshake e.g. Web Services. And Servers are _always_ authenticated. Clients can be *optionally* authenticated. When both servers and clients provide certificate to prove their identity, then it is referred as mutual TLS `mtls`. Another interesting point, server always presents certificate. And as you learn somewhere, certificate is nothing but a public key signed by someone including yourself or more appropriately Certificate Authority.

### Certificate Authority

Trust Anchor is a concept where client trust Certificate Authority and If CA has signed the certificate of the Server, then Client automatically accepts Server as authenticated entity.

## Chapter: 06 SSl/TLS Versions

### SSL History

SSL3.0 is complete redesign and was everywhere used till 2014. 2014 `PODDLE` proved you can see details in encrypted sessions. SSL3.0 is however also foundation for TLS till version 1.2 but TLS 1.3 is fully redesigned. In short some weakless was carried from SSL3.0 till TLS 1.2
To add further, TLS1.0 is basically SSL3.1 or one could say it is a minor version of SSL 3.0
SSL3.0 also introduced Certificate Chain Feature
Optional Support for additional key exchange protocol was introduced.

### TLS1.x History

In TLS1.0, HMAC was introduced. Now MAC stands for Message Authentication Code and Not for Media Access Control :) And additional Key Exchanges support was provided
TLS 1.0 and TLS 1.1 are deprecated in March 2021. Now TLS 1.2, AEAD is introduced. Authenticated Encryption with Associated Data. This means both Authentication and Encryption happens in a single step. AEAD is cipher.

In TLS 3.0, 

1. Forward secrecy and AEAD Cipher are **required**.
2. There is no focused toward backward compatibility. So weakess is not carried over.
3. All Insecure algorithms are removed.

Example of various Extensions

```bash
# below is the example where we have key usage and extended key usage for a CA.
X509v3 Key Usage: critical
    Digital Signature, Certificate Sign, CRL Sign
X509v3 Extended Key Usage: 
    TLS Web Server Authentication, TLS Web Client Authentication
```
