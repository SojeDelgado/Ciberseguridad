#### Description

In RSA, a small `e` value can be problematic, but what about `N`? Can you decrypt this? [values](https://mercury.picoctf.net/static/bf5e2c8811afb4669f4a6850e097e8aa/values)
#### Solución
``` bash
┌──(kali㉿kali)-[~/Downloads]
└─$ python3          
Python 3.11.4 (main, Jun  7 2023, 10:13:09) [GCC 12.2.0] on linux
Type "help", "copyright", "credits" or "license" for more information.
>>> from Crypto.Util.number import long_to_bytes
>>> from Crypto.Util.number import inverse
>>> c = 421345306292040663864066688931456845278496274597031632020995583473619804626233684
>>> e = 65537
>>> p = 1461849912200000206276283741896701133693
>>> q = 431899300006243611356963607089521499045809
>>> n = p * q
>>> n
631371953793368771804570727896887140714495090919073481680274581226742748040342637
>>> tn = (p-1)*(q-1)
>>> d = inverse(e,tn)
>>> m = pow(c,d,n)
>>> m
13016382529449106065927291425342535437996222135352905256639647889241102700065917
>>> long_to_bytes(m)
b'picoCTF{sma11_N_n0_g0od_55304594}'
```