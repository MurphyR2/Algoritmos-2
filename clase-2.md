# Clase 2

## Equivalencias

```
a=5
a+=3 # a=a+3
print(a)

b=7
b/=3 #b=b/7
print(b)

##-------------------------------Utilizando cadenas ----------------------##

var1="uni"
var1+="versidad"
print(var1)
```
## While

```
##---------------Condicion While---------##

##s=1+3+5+7+...+ (2n-1)
n=int(input("Ingrese el numero de terminos: "))
contador=1
s=0
while(contador <=n):
    term=2*contador -1
    s+=term
    contador+=1
print("El numero de terminos {0} es: {1}".format(n,s))
print(f'La suma de terminos es: ',s)
```

## Break  

```
##---------------Break ---------##
cad1="Universidad"
i=0

while(i<len(cad1)):
    print(cad1[i],end=" ")
    if(cad1[i]=='e'):
        break
    i+=1

```
## Continue
```
cad2="Electronica"
j=-1
while(j<len(cad2)-1):
    j+=1
    if(cad2[j]=='o'):
        continue
    print(cad2[j],end=" ")
```
## Pass
```
cad3="Telecomunicaciones"
k=0
while(k<=len(cad3)-1):
    if(cad3[k]=='u'):
        pass
    print(cad3[k],end=" ")
    k+=1
```
