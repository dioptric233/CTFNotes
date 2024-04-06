# RSA基础加解密(pqe)
 通过buu rsa1一题写出脚本

 ```
import gmpy2
from Crypto.Util.number import *

def main():
    p=
    q=
    dp=
    dq=
    c=
    mp=pow(c,dp,p)
    mq=pow(c,dq,q)
    p_q=gmpy2.invert(p,q)
    m=((mq-mp)*p_q % q)*p+mp
    print(hex(m))
        
if __name__ == "__main__":
    main()
 ```
dp泄露的原理 https://blog.csdn.net/MikeCoke/article/details/106095234 

再通过十六进制转化为字符串