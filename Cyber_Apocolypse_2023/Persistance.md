# Persistance
#HTB_CTF #Cyber_Apocolypse_2023
#Silent_Tilted 

**Prompt**
```
Persistence

Thousands of years ago, sending a GET request to /flag would grant immense power and wisdom. Now it's broken and usually returns random data, but keep trying, and you might get lucky... Legends say it works once every 1000 tries.
```

For this flag my approach was in a for loop that appended the output of my GET request to a text file. In order to loop my command I created a for loop 
```bash
for i in ‘seq 1 2002’; do command >> output; done
```

**![](https://lh6.googleusercontent.com/1w0wpNawWcydK4n1ey8idOd71cC1BXloSm-caj0cPsUIm3u1CSkAZnEB7u5afTRJUIfVBQVJvwmDseqMpovAFofFSro-mBf_I0N6H_FetdUoLjZbDxUWfueJ8YfBY0ryMXiUTuqyNeBfhA_V06P-ZtY)**

After gathering all the requests I just had to search through the Get_Out.txt I created.
```bash
cat Get_Out.txt | grep HTB
```

**![](https://lh4.googleusercontent.com/UMmCIkSKGya5zO_aQb2vO6sWnqXCLxRCNEobeEM7AZtZPYPyKl_qKXUybRmJiwVuAAy_Uuvn77_HGyFOly8qvAZooooUiGoJ5rFxU2Yk1OPmsvrIkvXC1DtDlX841Amd4s0xhpVlqY11vNtV_sJ1-8g)**

```
HTB{y0u_h4v3_p0w3rfuL_sCr1pt1ng_ab1lit13S!}
```
**HTB{y0u_h4v3_p0w3rfuL_sCr1pt1ng_ab1lit13S!}**
