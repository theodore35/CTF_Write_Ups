# Critical Flight
#HTB_CTF #Cyber_Apocolypse_2023
#Silent_Tilted

**Prompt**
```
Critical Flight

Your team has assigned you to a mission to investigate the production files of Printed Circuit Boards for irregularities. This is in response to the deployment of nonfunctional DIY drones that keep falling out of the sky. The team had used a slightly modified version of an open-source flight controller in order to save time, but it appears that someone had sabotaged the design before production. Can you help identify any suspicious alterations made to the boards?
```

The challenge had a series of Gerber (.gbr) files so I opened them all as layers using Gerbv
**![](https://lh5.googleusercontent.com/if01qA3B0orUUxTdoyQYJ_7aFTc5WP_vAjanJ-2Njcjl42dlxl-I2Edv6KdZQDZB9hGaMnrFMQWq6LVRkOi84s5-dOp81N5tFVuh58afkaAzJ_G_5lRmHlfozryRaVhNmjtodmuPJQ1EH_Aq4-Va0cQ)**

I noticed that there were portions of the flag written on certain layers, so after highlighting and isolating them it revealed 
**![](https://lh6.googleusercontent.com/Eo7Hs8ZCWoGYBvQMHQ8a1DuB2NenjImtMiKhG-Z8vKZvKOukNVOOnrDQM8t5M-4HxUs2N4wOcX1VQY5j-IZTgFpAjeHajHZ-tKIEYIligbObq_C-kD9n_ICLtJpq80kxqpdVWOYlkGLNqUn007zNIMg)**

```
HTB{533_7h3_1nn32w02k1n95_0f_313c720n1c5#$@}
```
**HTB{533_7h3_1nn32w02k1n95_0f_313c720n1c5#$@}**

