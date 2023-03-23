# Needle in a Heystack
#HTB_CTF #Cyber_Apocolypse_2023
#Silent_Tilted

**Prompt**
```
Needle in a Haystack

You've obtained an ancient alien Datasphere, containing categorized and sorted recordings of every word in the forgotten intergalactic common language. Hidden within it is the password to a tomb, but the sphere has been worn with age and the search function no longer works, only playing random recordings. You don't have time to search through every recording - can you crack it open and extract the answer?

```

Attached was a document, opening in mousepad++ I was able to simply use the find feature to grab the flag

**![](https://lh5.googleusercontent.com/Py6FOBaM5AhZItg22b0gTjMfJBmmrIgXU7kLxV2BHmW3aASD8EZKN1B3z_xwxYF1fnQxDRQDqbf5ZKRukwHf1fNCcrJYm2Z_t8CJyQ5xF9s0bmJEbzLsGiKtCyf6kDViAunNIL7NpRs43z2YPhGbWgw)**

Alternitively you could use grep in the command line
```
cat haystack | grep -a HTB
```

**![](https://lh4.googleusercontent.com/xP3GI0NnnUxEjfinzy5WjglWfF8kslCzDtQoLJl8zvV4VwKNpDNzW6CdCyOQHNg9058oc2e5FxOAzR3w6o68A5-ysQn2tT6e62X-wkL6NXIDrVghchHY6RhXl8PU19ltlyDeT2MTR4vA6RFZ63TCA4w)**

```
HTB{d1v1ng_1nt0_th3_d4tab4nk5}
```

**HTB{d1v1ng_1nt0_th3_d4tab4nk5}**