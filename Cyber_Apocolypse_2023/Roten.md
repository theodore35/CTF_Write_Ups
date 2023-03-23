# Roten
#HTB_CTF #Cyber_Apocolypse_2023
#Silent_Tilted

**Prompt**
```
Roten

The iMoS is responsible for collecting and analyzing targeting data across various galaxies. The data is collected through their webserver, which is accessible to authorized personnel only. However, the iMoS suspects that their webserver has been compromised, and they are unable to locate the source of the breach. They suspect that some kind of shell has been uploaded, but they are unable to find it. The iMoS have provided you with some network data to analyse, its up to you to save us.
```

Starting off there is an attached .pcap file. We can open this in wireshark to look for strange data.

We can filter the data for Web based infection traffic such with:
```
(http.request or ssl.handshake.type == 1) and !(udp.port eq 1900)
```

After quickly looking through, I identified fuzzing (sending requests to try and brute force the location of a directory)
**![](https://lh6.googleusercontent.com/GC8bK0DdrZdc4ZRLYZt9M2fgvyBZp37DwEzoyd0qouttL3fEWwdfBlDTGDH4RDB3tAbPMpVfj5QN7Ww16uhe2r6ZwYk1irMgoaHBn9k_PIL2sa06WqJq5ApIhFeRJRA0kLW66Irk45nByjpuUqgPRbE)**
In the image above we can see that the attacker is trying to brute force the location of “galacticmap.php” 

Now that we know that galactic map is suspicious, we can look for the first instance and export that file out.
**![](https://lh5.googleusercontent.com/R4Jl9SqKokeWY5nHBS6wP4B6L-F1KFNClbISKwkdvY2gdwtWtIcgCL9o9YNijnVadszVkpZrrFQQhs-nWhtTBhTpoGsgm4_Ig6jdzYEE3qQxc2GGq0QGXDtscHYI5nENh0TJjk1EEznQKE6YMreX_oA)**

below is the payload, and it is obfuscated to make it harder to read.
**![](https://lh3.googleusercontent.com/b6mkVzqu743tENUCaP4IU_YXvp0Tv-xW-OQBZiDVcFA0LNngR9ezjF1CEhzbZrijBW8tcm72RfOxnO91RFkEZxKBnU5xRulhnrwZEM_CetDkNB3eXxUnL_DW6Tf1gBkn_M8dd0Ki3aKPQKPwPxCW8Qk)**

At the end of the payload there is an eval argument, which will clear out any comments from the code
**![](https://lh5.googleusercontent.com/z7vHeEm_zn66MIfTCeF3C2MEdGSEI7IYuxH4eDBCP3ocjABpvpmzTtHZFMpKEmZ0nhQ49y-d0uoojfwbL-7GmAOVsXWyjm8hYfuMd3ev2eaONGE8o1Spamof09SiF-OFBKQ-RDTW3zKgbF_Rb4l__1w)**

In order to pull the raw data we can switch the eval() argument to echo.
**![](https://lh3.googleusercontent.com/qr4KrSPr5Sg6lHONh4c5wsOm_0L8VV9QPkZGNFdY1blhrvVONsNkNF33tgKkJAUU59pQjq8C83WzAcVCvN__XhKMSl7TXn5Y4J_02hXvrvGp7mOoEzCyY91pJodzol0nOQgKlr6_JeSjA-Z0SGGWaD0)**
And there is the flagg commented out 

```
HTB{W0w_ROt_A_DaY}
```
**HTB{W0w_ROt_A_DaY}**

