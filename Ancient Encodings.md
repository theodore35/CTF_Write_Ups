# Ancient Encodings
#HTB_CTF #Cyber_Apocolypse_2023
#Silent_Tilted

**Prompt**
```
Ancient Encodings

Your initialization sequence requires loading various programs to gain the necessary knowledge and skills for your journey. Your first task is to learn the ancient encodings used by the aliens in their communication.
```

Taking a look at the source we can see that the flag is encoded in base64 and then to hex
**![](https://lh4.googleusercontent.com/yDKY8naD2wkcIw6BERKYWay0h4M63iXg-m9CSKYI8AaP-HCV2i2VxZdu1-hMotbsXOnkoKZNwJyrW00_rjOkpMHMjWQrEV5FqHNrlix61Wnkaz0vsM6s79SoxzPDgbJsx3TelVPGBJYkALiiGqN6nnc)**

Attached documents included an Output.txt which held


Using Cyber chef we would need to work in reverse, so first to take our flag from hex, and then from base64
**![](https://lh5.googleusercontent.com/qxv6XD5kLLtpqZ5K47oI8Ic-GRn-IRzRxf8dWZhl4Njs5CqbyrLYCXqtC-GlM3zDeu5hCqPNlfNQvgEpfz9P8iS1pauTGHln4uDpGwUrYOEoomy50Qbw0JegB95tL0K0Bx9h-HMIJg_8hdUc7WPg90I)**

```
HTB{1n_y0ur_j0urn3y_y0u_wi1l_se3_th15_enc0d1ngs_ev3rywher3}
```
**HTB{1n_y0ur_j0urn3y_y0u_wi1l_se3_th15_enc0d1ngs_ev3rywher3}**