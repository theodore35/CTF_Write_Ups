# Questionnaire
#HTB_CTF #Cyber_Apocolypse_2023
#Silent_Tilted 

**Prompt***
```
Questionnaire

It's time to learn some things about binaries and basic c. Connect to a remote server and answer some questions to get the flag.
```

This flag was revealed after a series of questions. The first thing I did was initiate the docker.
```
nc <address> <port>
```

**![](https://lh6.googleusercontent.com/8oIpihLIQC0NwtMdwYbOOXj2K4byo-djPrZu6P1-Y68E18zCu_cbcpO7IJpyCnnaBeXS7DhucRuO_9ba_vE4DrQxaQXJwoBESCtwTrvH0qOV1tlZzK-MqLbicDuxhkI7BuPyo4iWdKuwL8unciWTG0A)**

This brings up the start page
**![](https://lh6.googleusercontent.com/E7xXEc9-HzGDPpUa9X1Y0iwb8CbFwL5rha_9tf_9OHahSYKd8hDP60ZjyNtF-w_98IvSl9Gvh_U1bn5otlRKfaXrNWCvuCvgL5acKi4v4pIq3YB8UgDMqBaErooRszc2iQszKPrsuay9hi1aIfU1IdI)**

And below, The first question is answered after checking the file information of test
**![](https://lh4.googleusercontent.com/LvzRkaDhCYSaxl9jPvnmew_MXz-PukmhmBM5t7eKazqY0UnwBjoT5I3qDBDIkE-FJOq3pG5Pc-RdFfmA_CsZacrK4LXtmn2WDF4D209GJDQj96HnP8dkINhSl38QBvhC2DGmdYhg9W14wVSut8qQlDA)**

Still using file, we are able to tell that it is also dynamically linked
**![](https://lh3.googleusercontent.com/25fHE7m6TBizKLZUS934fJPh9SGjz7KZ8apB6bdmPYl6yd7YFWODZ3pCRjCyO4eS4ss4lu3YhWN09BNTo2delBnNHsWs2hQK4plebq0lWmff4QnPTFfJnlriJ9y5Yv0qjOoEdFBL3sLnKJOtVuZ5v9k)**

Using file, we can also see that it is not stripped
**![](https://lh3.googleusercontent.com/s0YOUhiLfdMZn9vvwx6WWIz9G-qhlNz0-E6Ycn8nLyKsaVA55aBy9LS5bkllR1YJ_SnfJec2aik94uzGdBjix81KRMGq6zjMAemgmmr-Vb8Lcvs7K4O4YPYSF4yHEfJA0e8punFOKtiHcUPxhqwXfK0)**

The next question is related to protection, we can check this using the gef debugger
**![](https://lh6.googleusercontent.com/OVICgeXVxiWDXLSpcnEHJtnNRTDxOovYYIiAAJl4jaKDJuKI18XnPtX2jdd2so0Bd2gCxDQcMNYJL-FjpLYR9AtzYZt9b3T4L1fcSshPW-hh3J_QHuAMsRrnt9R-IiSGsVrjRlELPPLMS5fKJZtxvkg)**

After completing these series of questions a new page is revealed
**![](https://lh4.googleusercontent.com/dUDYn02PLFCgrMRkv5RYlDpfQiE8yFUmptlH_K6SvO_U5wJ-elEhWyKGu65Q96AFa11n_FXzxmxqZwFhyD8yoOYi2qbFiumNQz74MzcEXA-FJZiMldQLGLy_iO7iLUDp-RDEVc5y44Xwf-PSewJlw4s)**

This next question references the source test.c, vuln() is a custom method/function called from main()
**![](https://lh5.googleusercontent.com/YhoXn6oNB3OV-Jwt4Y7tMCTSEBgrYEDqTAnTyzHHi5k489iEeISQ1EBVHXoz8S4wKoihdFRDPb0t3nhzug-SdEU2KEdG8MxzC11F2WnKBiTytYr6NjPDxD0s8mNifHrAmZcezEgZQToGRFS4W8JyfB0)**

Using the source, we can see that char buffer is limited to "[0x20]"
**![](https://lh4.googleusercontent.com/V1GfBgWJJwmHsCXEkjsIPd4da88ijlN24ltf1cQa51p54h47xUnBguSXof-1i5fmV3pj_SS7hByFrUumSjYe-hwEk5ncWRYW6u8Vi-CYagxaEmHv5Z9I4yRepAGyZVnC_KBOeWFj1WkRDDpfMAmBUH4)**

There is a custom function that is never specifically called, gg()
**![](https://lh5.googleusercontent.com/ro2GeoRIkl1Vg_PqxBHA7wKRM3BdV7yKw4ZEwumd1OvpOTPs6x0LvPs1xRX9ZUit3htUuvOjww-oawSHi1DeD3xc0bOzoY_RqbspMt556Ok8Gs67MyfESRICkMErRzwg6AR7PxiTHuKBT5x1W9EWmmM)**

After answering this question another page is loaded
**![](https://lh5.googleusercontent.com/vwjzq8SsraFwuSO3zblaLjVNoi7HhpujK4mjFfAor1r5fJet12F3EtIp2-3l473uzTgviitOqxg-MRdgu1nLHcd0ZclxiWSOUP0oitqgqZ3iFCC01cTZqskA2MfP9w-eCOqCtWJxjXjnPQQTqQ7CtIA)**

This next question asks which function could trigger a buffer overflow, in this case, it is fgets
**![](https://lh5.googleusercontent.com/cZ8oon4r2W_qgKyhkGrOqEb4BcQBCmzs5mXSUgbHbaehR0T_sQX6YuZ8e3QkPDEqd2QWiDLQFhvc1JEjty-j38cfS14-kei4lyX7m5tQUXI5H-vz9OTVephNO6L2AZBGfknzlKUKMVd61SDv0wWo9RQ)**

After running the program we can see a byte segmentation fault at 40 ‘A’s
**![](https://lh3.googleusercontent.com/eFd7KUh_E3pRaxyXNh0aKEvGRSDrqi-fdVCixuxrobbGHAk7UscGbPmSG6M05heeElJxZ1Mu0wv4BKBEZeZzQ-X72DLrAaXwc6OEWc0V3LlRdvZxVoQXAm8W2MHYfppFLY6r0Ronzt1jcSdfGswyek8)**

For those wondering what happens when you create this fault, the method gg() runs and it prints the flag.txt “HTB{f4k3_fl4g_4_t35t1ng}”
The last question asks for the address of the method gg(), which you can get from the debugger
**![](https://lh5.googleusercontent.com/0weWgvKedu-ZKGmdGLY08ojkxpgLq2kPulgbD1J-_fu-ZdJcGqDCQivxam_okpWDYaonlK-0ovshL0W3L3yfrRZfGb9xGdNkePBPs_cM0XBevl5f4qpuh4OBR3zpRak6LKVfvvXLMnvhkqHSIZQg5wE)**

```
HTB{th30ry_bef0r3_4cti0n}
```
**HTB{th30ry_bef0r3_4cti0n}**

