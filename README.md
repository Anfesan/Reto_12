# Reto_12
```phyton
#Reto 12
file = open('C:\\Users\\anfes\\Downloads\\mbox.txt', "r")
vocal = 0
vocales=[]
consonantes=[]
consonante = 0
lista_palabras=[]
lista_unicas=[]
lista_conteo=[]

for line in file.readlines():
  vocales=map(line.lower().count, "aeiou")
  vocal+=sum(vocales)
  consonantes=map(line.lower().count, "bcdfghjklmnpqrstvwxyz")
  consonante+=sum(consonantes)
  lista_palabras=line.lower().replace('.,:-"\n"',' ').split()
  for i in lista_palabras:
    if i not in lista_unicas:
      lista_unicas.append(i)
      lista_conteo.append(1)
    lista_conteo[lista_unicas.index(i)]+=1
for j in range(0,49):
  current_max=lista_conteo.index(max(lista_conteo))
  print(lista_unicas.pop(current_max))
  print(lista_conteo.pop(current_max))
    

file.close()

print('Total Vocales : '+str(vocal))
print('Total Consonantes : '+str(consonante))

```
1. Cantidad de vocales 
2. Cantidad de consonantes
3. Listado de las 50 palabras que más se repiten
```phyton
2007
20414
from
18127
by
18029
received:
16174
with
12757
id
12608
-0500
11775
dec
9268
nov
8989
for
7715
esmtp
7189
paploo.uhi.ac.uk
7189
nakamura.uits.iupui.edu
7189
<source@collab.sakaiproject.org>;
5392
text/plain;
5392
charset=utf-8
5392
+0000
4933
(gmt)
4933
oct
4165
you
3622
murder
3595
(cyrus
3595
lmtpa;
3595
(localhost
3595
[127.0.0.1])
3595
(postfix)
3595
smtp
3595
date:
3588
thu,
3535
tue,
3306
fri,
2965
-0400
2911
to
2768
mon,
2705
wed,
2583
the
2545
svn
2529
-
2038
2007)
2033
modify
1885
new
1878
this
1878
message
1840
was
1835
29
1835
sakai
1824
at
1823
using
1822
can
1822
Total Vocales : 1597835
Total Consonantes : 2612121
```
