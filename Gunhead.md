# Gunhead
#HTB_CTF #Cyber_Apocolypse_2023
#Silent_Tilted 

**Prompt**
```
Gunhead

During Pandora's training, the Gunhead AI combat robot had been tampered with and was now malfunctioning, causing it to become uncontrollable. With the situation escalating rapidly, Pandora used her hacking skills to infiltrate the managing system of Gunhead and urgently needs to take it down.
```

Pulling up the webpage we are greeted with a few tools and views
**![](https://lh5.googleusercontent.com/IGexbtLkAAPsxh84JJMRrk56eFkKArbSo59yBxVSRQBsipZQSmEnJG5rLNEUMUItIDm_4q4bQv_l1IWwqddI07Zxyh8D6xIcWItwp0A0gw5lgtHAvoOZjsiQJQiCpZlbz1Xw_gKIrbXu0DwoyL0XHHY)**

**![](https://lh3.googleusercontent.com/-L5fWe0b5RdQgisQlR0AkgfIxw0M_xZqDh4Jedwbk3q-Pznn98OtGZEXDXc7ZkC8n3FNiwWhN2YHdSmBDrnNHMz47l8XqxKsY5wBoCq6uJlNts3MkK2tdXLXpR349RtC-pQDVuTl9-zm77s3OjpKYbU)**

The challenge also provides some files alongside the docker. Exploring some of these reveals that the /ping command has unfiltered input.
**![](https://lh3.googleusercontent.com/p0vh5FfE8qPo9SHNQLc6s_9jjmKhwgy6DdEWecoehVTgx6YqWquLiAvXXqt6DqZwVoS5HTwU3WIsPt4wFq4EkeMbHfoZYVhb6g2QqeDHyUh48B5b03Cs5ggIHdqBP22eDS9hoLV7H_ak8ODJCWNRFhE)**

We can use this unfiltered input in order to search through the directories using the absolute path and then print the flag.
**![](https://lh6.googleusercontent.com/eeEcxbDb2qXBbJM2Ff-nu_A6Gbj8VWIMPuNefHdag3aalVXovs-4XXK0m737vanZph05psrdeOziql0DUXXpOo8FiLhOQZQTNRtxi1yRHUvgnerScxAblYlZiCB1SkN95L-qLUhKlZ99jbr4Q-isD3k)**

```
HTB{4lw4y5_54n1t1z3_u53r_1nput!!!}
```
**HTB{4lw4y5_54n1t1z3_u53r_1nput!!!}**