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

## Lista por compresion

```
L=[[1,2,3],[4,5,6]]
for element in L:
    print(element)
L=[1,2,3,4,5,6,7,8,9]
L6=[elem[0] for elem in L]
print(L6)

L7=[i*i for i in range(10) if i%2!=0]

print (L7)
```
##Funciones

```
def verificarSiPrimoNo(num):
    ac=0
    for div in range(1,num+1):
        if(num%div==0):
            ac=ac+1
    if(ac==2):
        return 1
    else:
        return 0
nx=int(input("Ingrese numero: 13"))
val=verificarSiPrimoNo(nx)
if(val==1):
    print("Es Primo")
else:
    print("No Primo")
```
