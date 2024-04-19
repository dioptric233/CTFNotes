# RSA基础加解密(pqe)
 通过buu rsarsa一题写出脚本

```
import gmpy2
def main():
    p=
    q=
    e=
    n = p*q
    d =gmpy2.invert(e,(p-1)*(q-1))
    choice = input("加密(1)还是解密(2)")
    if choice == "1":
        C = int(input("明文"))
        M = pow(C,d,n)
        print(M)
    elif choice == "2":
        m = int(input("密文"))
        C = pow(m,e,n)
        print(C)     
if __name__ == "__main__":
    main()
```
