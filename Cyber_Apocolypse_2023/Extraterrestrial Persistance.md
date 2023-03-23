# Extraterrestrial Persistance
#HTB_CTF #Cyber_Apocolypse_2023
#Silent_Tilted 

**Prompt**
```
Extraterrestrial Persistence

There is a rumor that aliens have developed a persistence mechanism that is impossible to detect. After investigating her recently compromised Linux server, Pandora found a possible sample of this mechanism. Can you analyze it and find out how they install their persistence?
```

Downloading the file I opened it in Visual Studio code, here is a snippet
**![](https://lh5.googleusercontent.com/jpaNSHp5VqDHZq637bDDKlTPGaE4MG1KUk76VggIPlM0LzC0pNwnf78lNC2f1vGG-efPU58Vc50jas4I2cS_eMhV6XPJ1ChUJwniBpiI90XGUhT48y8JomeXrh8f_Ot9yLIiWqsO6CWELICvIsWeqfg)**

I saw that there is a very long portion and then at the end it decodes it from base 64
**![](https://lh5.googleusercontent.com/3tMZ4apE0K2avImKUZgR92vfN9T2Nt21Q3k-p0nF7YcuoVeS8zDVTK3oWJcRHMA9o_CZ1WPpghze_M6bP8aOzI4wgiv1yJhXi7i7RT0Lk5L60wyIZMOTzMq_KCsRjp7Gdn5mFTLJ4RGDExPe1Fo9eGk)**
After putting that portion into cyberchef and decoding from base 64 the flag is revealed
**![](https://lh4.googleusercontent.com/UFnMyDFc8lcNVxZi4nuIoLIE6_f09YBHsDxANrA0gSf5johdjZD_76XFjGhwbPUS_JI9M2YbbwDZ4DCdKCYWiigkRPMSXKeD2h8BKSNsRwlABrvfXX6PYDXAcRMS1cq1HR_P8OGWE4CBDflSuRSnCjU)**

```
UhUQnt0aDNzM180bDEzblNfNHIzX3MwMDAwMF9iNHMxY30
```

```
HTB{th3s3_4l13nS_4r3_s00000_b4s1c}
```
**HTB{th3s3_4l13nS_4r3_s00000_b4s1c}**
