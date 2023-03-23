# Alien Cradle
#HTB_CTF #Cyber_Apocolypse_2023
#Silent_Tilted 

**Prompt**
```
Alien Cradle

In an attempt for the aliens to find more information about the relic, they launched an attack targeting Pandora's close friends and partners that may know any secret information about it. During a recent incident believed to be operated by them, Pandora located a weird PowerShell script from the event logs, otherwise called PowerShell cradle. These scripts are usually used to download and execute the next stage of the attack. However, it seems obfuscated, and Pandora cannot understand it. Can you help her deobfuscate it?
```

Opening the file in mousepad on my kalibox shows this powershell script
**![](https://lh5.googleusercontent.com/jAoAx-tuFW7Si_klcD96ZdpjoZH1QcLRZ0EYqn9KdSK8men_IfE08ThK6FKTVocTCmNhIsakikbnVxJQD3kWt5eJ64Wz6K1JtPiEEtAfsWlAPIbAAmZGgvdkiz8Ny_66DqLvv_r_5_PsUg_FsHLsleM)**

You can see the string listed in the file broken up.
```
'H' + 'T' + 'B' + '{p0w3rs' + 'h3ll' + '_Cr4d' + 'l3s_c4n_g3t' + '_th' + '3_j0b_d' + '0n3}
```

```
HTB{p0w3rsh3ll_Cr4dl3s_c4n_g3t_th3_j0b_d0n3}
```
**HTB{p0w3rsh3ll_Cr4dl3s_c4n_g3t_th3_j0b_d0n3}**
