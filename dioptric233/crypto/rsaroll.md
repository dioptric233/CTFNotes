# RSA基础加解密(more one n)
 通过buu rsaroll一题写出脚本

 ```
import gmpy2

n = 
# 分解得到p q
p = 
q = 
e = 
phi_n = (p-1) * (q-1)
d = gmpy2.invert(e, phi_n)
m = ""

c = []

for i in range(len(c)):
    m += chr(gmpy2.powmod(c[i], d, n))
print(m)


 ```