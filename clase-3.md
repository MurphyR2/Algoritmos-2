```
L=[4,98,11,3,5,690,30,2,6]
print(L)

L1=sorted(L) ##ascendente
print(L1)

L2=

L3=[4,98,11,3,5,690,30,2,6]
L3.sort()
print(L3)
L3.sort(reverse="True")
print(L3)
```

```
L=["Rosa","Maria","juan","Benito","Juan","ana","Lee"]
print(L)
L.sort()
print(L)
L.sort(reverse=True)
print(L)
L.sort(key=str.lower)
print(L)
L.sort(key=str.lower,reverse=True)
```

```
L=[["maria",19],["pepito",14],["juan",15],["pepe",20]]
print(L)
L.sort(key=lambda alumnoNota:alumnoNota[1],reverse=True)
print(L)

L.sort(key=lambda alumnoNota:alumnoNota[0])
print(L)
```
