# MD5加密爆破（已知部分密文）

仅未知密文中的部分字符时使用
```
import hashlib
#print hashlib.md5(s).hexdigest().upper()
k = 'TASC?O3RJMV?WDJKX?ZM'
for i in range(26):
    temp1 = k.replace('?',str(chr(65+i)),1) #用ascii开始，从A开始查
    for j in range(26):
        temp2 = temp1.replace('?',chr(65+j),1)
        for n in range(26):
            temp3 = temp2.replace('?',chr(65+n),1)
            s = hashlib.md5(temp3.encode('utf8')).hexdigest().upper()#注意大小写
            if s[:4] == '':#检查元素
                print(s)
```