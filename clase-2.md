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
## For

```
for i in range(1,15):
    print(i,end=" ")
    
for i in range(1,31):
    print(i,end=" ")
    
for i in range(1,31,4): #for con paso 4
    print(i,end=" ")
```
### Ejercicio
1. Calcular la suma de la siguiente serie con x=1 hasta que el n-término sea mayor a 0.0001

    e<sup>x</sup>=1 + x<sup>2</sup>/2! + x<sup>3</sup>/3! + ... + x<sup>n</sup>/n! = 2.7




```
import math as mt
e=0
x=1
cont=0
term=1
while(term>0.0001):
    fact=mt.factorial(cont)
    term=(mt.pow(x, cont))/fact
    e=e+term
    cont+=1
print("El n-termino es:",term,end="\n\n")
print("La suma es e =",e,end="\n\n")
```
2. Ingresar n numeros y mostrar la suma de los mismos hasta que ingreses el valor de -1 donde el programa termine


## Listas

Son mutables (sus valores y longitud pueden cambiar)

```
L3=[18,19,20,"Testla,[1,2,3],"Fisher",123]
print(L3)
print(L3[0])
print(L3[6])
print("--------------Inversa--------------\n")
print(L3[-1])
print(L3[-2])

print("---------------Longitud de lista------------\n")
print(len(L3))

print("---------------Cambio de valores------------\n")
L3[2]="Dirac"
print(L3)

print("--------------Operadores con listas---------")
L1=[4,5,6]
L2=[2,3]
L4=L1+L2
print(L4)

L5=L2*3
print(L5)
```
Agregar elementos a lista
```
print("-------------------Agregar elementos a la lista------------")
#append 
#insert
#extend
L6=["circuitos",[2,3,4],16,"electronicos"]
print(L6)

L6.append("Antenas")
print(L6)
L6.append([18,19,20])
print(L6)

print("-------------------Insert----------------")
L6=["circuitos",[2,3,4],16,"electronicos"]
print(L6)
L6.insert(3,"vacaciones")
print(L6)
print("-------------------Extend----------------")
L6=["circuitos",[2,3,4],16,"electronicos"]
print(L6)
L6.extend([10,15,17,"5G"])
print(L6)
```
Eliminar elementos
```
L7=["Tecnologia","Energia",12,70,30,[5,6,7],100,200]
print(L7)

print("---------------del------------------")

del L7[1]
print(L7)
del L7[3]
print(L7)

print("-------------remove--------------")
L7=["Tecnologia","Energia",12,70,30,[5,6,7],100,200]
print(L7)
L7.remove("Energia")
print(L7)

print("--------------pop----------------")
L7=["Tecnologia","Energia",12,70,30,[5,6,7],100,200]
print(L7)
L7.pop()
print(L7)
L7.pop(1)
print(L7)
a=L7.pop(3)
print(a)

#Transferir a otra lista
L7=["Tecnologia","Energia",12,70,30,[5,6,7],100,200]
L8=[]
L8.append(L7.pop(5))
print(L7)
print(L8)

```
### Referencias y Copias de listas

Ambas listas están almacenadas en la misma posición de memoria
```
print("----------Referencia------------")
L9=[20,70,"Galois",888,[2,4,5]]
print(L9)
L10=L9
L10.append(10000)
print(L10)
print(L9)
```
```
print("----------Copia---------------")
L11=L9[:]
L12=L9.copy()
print(L12)
L12.append([1,7,4])
L12.append("Newton")
print(L11)
print(L12)
print(L9)
```

### For con listas

```
Lx=[4,7,9,1,20,100]
print(Lx)
for elem in Lx:
    print(elem,end=" ")
print("\n")
for indice in range(len(Lx)):
    print(Lx[indice],end=" ")
```
### Ejercicio

2. Programa que suma los términos hasta que se ingrese -1

```
#Segundo ejercicio

#Programa que suma los terminos hasta que se ingrese -1
s=0
n=int(input("Ingrese el numero de terminos: "))
cont=1
while(cont<=n):
    term=int(input("Ingrese el termino: "))
    if(term==-1):
        break
    s+=term
    cont+=1
    
print("La suma hasta {0} es: {1}".format(term,s),end="\n")
```

3. Programa que suma los elementos de una lista
```
#Tercer ejercicio

#Programa que suma los elementos de una lista
n=int(input("Ingrese el numero de elementos: "))
L=[]
for i in range(0,n):
    x=int(input("Ingrese el elemento: "))
    L.append(x)
suma=sum(L)
print("La lista es: {0} \n\n La suma de sus elementos es: {1}".format(L,suma))
```

4. Continue: Ingresar desde un numero que te permita encontrar las divisiones exactas y se salta cuando se divide entre 0
```
#Cuarto ejercicio

#Ingresar desde un numero que te permita encontrar las divisiones exactas 
#y se salta cuando se divide entre 0


L=[4,3,0,8,9]
print(L)

num=int(input("Ingrese el numero: "))

for element in L:
    if(element==0):
        continue
    div=num/element
    print("{0}/{1} = {2}".format(num,element,div))
```
