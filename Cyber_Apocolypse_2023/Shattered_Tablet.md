# Shattered Tablet 
#HTB_CTF #Cyber_Apocolypse_2023
#Silent_Tilted 

**Prompt**
```
Shattered Tablet

Deep in an ancient tomb, you've discovered a stone tablet with secret information on the locations of other relics. However, while dodging a poison dart, it slipped from your hands and shattered into hundreds of pieces. Can you reassemble it and read the clues?
```

To start off I decided to run the program attached with Ghidra on DogBolt 
https://dogbolt.org

**![](https://lh6.googleusercontent.com/SOMafbCuZy83kya-EnOKrEgJXlzAD7hl48q31-jyTCJjW-pYlClkPd1Iu6E2Bq833OcP60LNizB2MMbwI7uOJEuWlK5Kgapih8R9x2rCAik3Os1KHmU1_j785Gu1aeXrczR2aBVXokv2w-oFo9UsNAE)**

This is a list of char used in the flag that we need to unscramble 
I noticed that the tablet’s variables are listed in order. So I deleted all the program related language from it leaving each number assignment to the characters.

**![](https://lh3.googleusercontent.com/YnEZco6k1WKd6b-WnJYjJamtA8f6rG3RauIohuSYZem2pdyhUVE4o6Ta5EDyaSb0WT6Z0f5LZyWkEK1i1Nls7E-rQ-hN4-GSht9sf9v6J2oVk7MT9soJ158qJDciRrKLuegEg2T-Y0kKio-YVNjpiUo)**

Next I replaced the numbers in order to make it sort in the correct blocks.

**![](https://lh3.googleusercontent.com/bDnq39FWqVlIkXY6YqlOT0fj5yUYekIfjWMdXz33auS2YOMXNG1OifE0DvXqgkSZiCFcyrVUSSFumN4wF6CQSNE5HZHJLbYb0VODZijiEDExkkcEVRdITfYQ1s8diPAtXIKKV-btqePxqI23NcFaBeg)**

```bash
sort listV2.txt
```

**![](https://lh5.googleusercontent.com/YzloPrq0394AxhBh7qPYVk65GT4S3A8lSMCE7s9cK9VrWCw3TLFD98Damuuf3Lh1J9wpcZvj3HIOL-T9HQd8eGdknaqSBjuNdDh4_ifEWSyI2rBQD7SroG7xwLJQTLQcdYrwy-Bvna5ukjUHpKEsaZg)**

Now all that is left is to extract the sorted lists characters!
```bash
sort listV2.txt >> listV3.txt
```

```bash
cat listV3.txt | awk -F\' '{printf $2}'
```

```
HTB{br0k3n_4p4rt,n3ver_t0_b3_r3p41r3d}
```

**HTB{br0k3n_4p4rt,n3ver_t0_b3_r3p41r3d}**

