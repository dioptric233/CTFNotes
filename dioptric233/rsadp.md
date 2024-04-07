# RSA dp泄露(pq dpe)
 通过buu rsa2一题写出脚本

 ```
import gmpy2

e = 
n = 
dp = 
c = 

for i in range(1,e):                   
    if(dp*e-1)%i == 0:
        if n%(((dp*e-1)//i)+1) == 0:   
            p=((dp*e-1)//i)+1
            q=n//(((dp*e-1)//i)+1)
            phi=(q-1)*(p-1)            
            d=gmpy2.invert(e,phi)         
            m=pow(c,d,n)               
           
print(m)                               
print(hex(m)[2:])                      
print(bytes.fromhex(hex(m)[2:])) 
 ```
dp泄露推导的原理 https://blog.csdn.net/MikeCoke/article/details/106095234
