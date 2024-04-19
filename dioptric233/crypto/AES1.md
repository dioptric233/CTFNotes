# AES解密


```
from Crypto.Cipher import AES
import os
c= b''
iv= b''
key= b''

my_aes = AES.new(key, AES.MODE_CBC, iv)
m = my_aes.decrypt(c)
file1 = open('flagout.txt', 'wb')
file1.write(m)
file1.close()
```