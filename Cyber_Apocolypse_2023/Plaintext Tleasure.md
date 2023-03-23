# Plaintext Tleasure
#HTB_CTF #Cyber_Apocolypse_2023
#Silent_Tilted 

**Prompt**
```
Plaintext Tleasure

Threat intelligence has found that the aliens operate through a command and control server hosted on their infrastructure. Pandora managed to penetrate their defenses and have access to their internal network. Because their server uses HTTP, Pandora captured the network traffic to steal the server's administrator credentials. Open the provided file using Wireshark, and locate the username and password of the admin.
```

Opening the file in wireshark i right clicked on the data to follow the TCP Stream, along stream 4 I found the flag
**![](https://lh3.googleusercontent.com/VMiTpnXkiTI_f8nWawa0LOc2fP99QBQTx1EStvmvgewsBcDmmhafj1S6UzuOZtwta6zhPzURjRLL4sPqsR61yI6hE3kAGn_KqI3ODviEjCpvrt5yfTBQkstVQja0BnqN1PsNDIg1K6iAfGd3xQZMMOM)**

```
HTB{th3s3_4l13ns_st1ll_us3_HTTP}
```
**HTB{th3s3_4l13ns_st1ll_us3_HTTP}**
