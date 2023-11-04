
### Solucion
```python
from pwn import *
r = remote("jupiter.challenges.picoctf.org", 18821)
print(r.recvuntil(b'):').decode())
r.sendline(b'Y')
print(r.recvuntil(b': ').decode())
q = 60413
p = 76753
n = p * q
print('n='+str(n))
r.sendline(str(n).encode())

print(r.recvuntil(b'):').decode())
r.sendline(b'Y')
print(r.recvuntil(b': ').decode())
p = 54269
n = 5051846941
q = n // p
print('q='+str(q))
r.sendline(str(q).encode())

print(r.recvuntil(b'):').decode())
r.sendline(b'N')

print(r.recvuntil(b'):').decode())
r.sendline(b'Y')
print(r.recvuntil(b': ').decode())
q = 66347
p = 12611
t = (p-1) * (q-1)
print('t='+str(t))
r.sendline(str(t).encode())

print(r.recvuntil(b'):').decode())
r.sendline(b'Y')
print(r.recvuntil(b': ').decode())
m = 6357294171489311547190987615544575133581967886499484091352661406414044440475205342882841236357665973431462491355089413710392273380203038793241564304774271529108729717
e = 3
n = 29129463609326322559521123136222078780585451208149138547799121083622333250646678767769126248182207478527881025116332742616201890576280859777513414460842754045651093593251726785499360828237897586278068419875517543013545369871704159718105354690802726645710699029936754265654381929650494383622583174075805797766685192325859982797796060391271817578087472948205626257717479858369754502615173773514087437504532994142632207906501079835037052797306690891600559321673928943158514646572885986881016569647357891598545880304236145548059520898133142087545369179876065657214225826997676844000054327141666320553082128424707948750331
c = pow(m, e, n)
print('c='+str(c))
r.sendline(str(c).encode())

print(r.recvuntil(b'):').decode())
r.sendline(b'N')

print(r.recvuntil(b'):').decode())
r.sendline(b'Y')
print(r.recvuntil(b': ').decode())
q = 92092076805892533739724722602668675840671093008520241548191914215399824020372076186460768206814914423802230398410980218741906960527104568970225804374404612617736579286959865287226538692911376507934256844456333236362669879347073756238894784951597211105734179388300051579994253565459304743059533646753003894559
p = 97846775312392801037224396977012615848433199640105786119757047098757998273009741128821931277074555731813289423891389911801250326299324018557072727051765547115514791337578758859803890173153277252326496062476389498019821358465433398338364421624871010292162533041884897182597065662521825095949253625730631876637
e = 65537
t = (p-1) * (q-1)
d = pow(e, -1, t)
print('d='+str(t))
r.sendline(str(d).encode())

print(r.recvuntil(b'):').decode())
r.sendline(b'Y')
print(r.recvuntil(b': ').decode())
p = 153143042272527868798412612417204434156935146874282990942386694020462861918068684561281763577034706600608387699148071015194725533394126069826857182428660427818277378724977554365910231524827258160904493774748749088477328204812171935987088715261127321911849092207070653272176072509933245978935455542420691737433
c = 15898528329836486259454280642537682745047492250031819804208947573732209296147142448425785475270839697919293976182333838349380319082449313123936042811917218253196274432195116911131311101664245124078266845291992250418272429673592762174381527121624558596357902629676671110003023710107905410987270486412752306303470410502366293287214002128769133995449197216690029130480234844827254205117539992852496638836353167147769854523276743309449394023887611024408163270210444112592577810624181267012402352918669635578760260278590557042623644240179185252741450067430771092134328724271261927055861090533852597204599189199436235384288
e = 65537
n = 23952937352643527451379227516428377705004894508566304313177880191662177061878993798938496818120987817049538365206671401938265663712351239785237507341311858383628932183083145614696585411921662992078376103990806989257289472590902167457302888198293135333083734504191910953238278860923153746261500759411620299864395158783509535039259714359526738924736952759753503357614939203434092075676169179112452620687731670534906069845965633455748606649062394293289967059348143206600765820021392608270528856238306849191113241355842396325210132358046616312901337987464473799040762271876389031455051640937681745409057246190498795697239
q = n // p
t = (p-1) * (q-1)
d = pow(e, -1, t)
m = pow(c, d, n)
print('m='+str(m))
r.sendline(str(m).encode())

print(r.recvall().decode())

flag = bytes.fromhex(hex(m)[2:]).decode()

print(flag)
```

picoCTF{wA8_th4t$_ill3aGal..o26cefcb2}