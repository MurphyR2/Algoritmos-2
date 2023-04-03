# Clase 1


<img src="/assets/python-logo-4k-i6.jpg" alt="Logo"  width="100%">

Ciclo:2023-1

Librerias de C++ importantes: Flaks,Quivi,ROS

```
print("Hola, mundo!")
````



# Herramientas
1. Anaconda Navigator
2. Spyder (Anaconda)
3. Jupiter (Anaconda)

## 1. Spider
1. Crear una carpeta para almacenar tus archivos D:\python_BMA20_M_
2. Buscar en la parte derecha superior de Spider la carpeta para que se guarde ahí.


```
print("{0} {1} {0}".format("Hola","Mundo"))
```

También puede imprimirse de la siguiente manera:
```
a=1
b=2
print("a=",a,"y","b=",b)
```
## 2. Jupiter
1. En Anaconda Navigator entrar a Jupiter Notebook
2. Darle en New -Python3 (ypykernel)

### Tipos de datos

En python se tienen los datos:

* String
* Int
* Float
* Booleanos
* Lista (list) : Sí se puede cambiar los valores
* Tuplas (tuple) : Son inmutables. No se puede cambiar ningún valor.
* Dictionario (dict)
* Conjuntos (set)



```
print("-------------------------------Tipos de Datos --------------------------")
a=14
print(type(a))
b=3.14
print(type(b))
c="Electronica"
print(type(c))
```

Inicializar listas:
```
d1=list()
e1=dict()
t1=tuple()
t2=set()

d2=[]
e2={}

print(type(d2))
print(type(e2))
```
Ejemplo de contenido de listas:

```
lista=[4,5,"UNI",[2,3]]
dict={"clave1":12,"clave2":13,"clave3":13,45:"clave4"}

print(type(lista))
print(type(dict))
```

### Operandos matemáticos
```
num1=7
num2=3

suma=num1+num2
resta=num1-num2
multi=num1*num2
div=num1/num2
cociente=num1//num2
residuo=num1%num2

round(div,2) #Redondeo a dos decimales
```

### Condicionales

Mayor, menor, igual

```
x1=7
x2=5
x3=3

r1=x1>x2>x3
r2=x1==x2>x3
r3=x1!=x2>x3
r4=(x1>x3)&(x2>x1) #Tener en cuenta los parentesis porque a veces la respuesta es incorrecta
r5=(x1>x3)|(x2>x1) #Para OR

print(r1,r2,r2)
```
If, elif y else
```
val1=int(input("Ingrese val1: "))
val2=int(input("Ingrese val2: "))
val3=int(input("Ingrese val3: "))
if((val1!=val2)&(val1!=val3)&(val2!=val3)):
    print("Distintos")
elif(val1==val2==val3):
    print("Iguales")
else:
    print("No todos son iguales")
```
### Entradas del usuario:
```
valor1=int(input("Ingrese valor1: ")) #Notar que convertimos a int
```

### Ejercicio
1. Ingresar un numero de 3 cifras y mostrar la suma de sus scirfras y ejecutar la respuesta en el prompt de Anaconda
```
numero=input("Ingrese el numero de 3 cifras: ")
print(numero)
suma=0
i=0
if(len(numero)==3):
    suma=int(numero[0])+int(numero[1])+int(numero[2])
    print("La suma es:",suma)
else:
    print("El numero no es de 3 cifras.")
```

Solución alternativa:

```
valor1=input("Ingrese valor1: ")
suma=0
for i in valor1:
    suma+=int(i)
print("La suma es:{0}".format(suma))
```

2. Crear un programa que resuelva una ecuación cuadrática con soluciones reales e imaginarias. Los coeficientes son ingresados por el usuario

```
#Programa que calcula las raizes reales e imaginarias de una ec. cuadratica
import math as mt

a=int(input("Ingrese a: "))
b=int(input("Ingrese b: "))
c=int(input("Ingrese c: "))

print("\nLa ecuacion es: {0}x^2+{1}x+{2}=0".format(a,b,c))
print("\n")

discriminante=b*b-4*a*c
if(discriminante>0):
    x1=(-b+mt.sqrt(discriminante))/(2*a)
    x2=(-b-mt.sqrt(discriminante))/(2*a)
    print("Las soluciones son reales y son: \n\nx1: {0}\nx2: {1}".format(x1,x2))
elif(discriminante==0):
    x1=(-b)/(2*a)
    print("Las solucion es reales y única: \n\nx1: {0}".format(x1))

else:
    realx1=-b/(2*a)
    imagx1=mt.sqrt(-1*discriminante)/(2*a)
    print("Las soluciones son imaginarias y son: \n\nx1: {0}+{1}i\nx2: {0}-{1}i".format(realx1,imagx1)) 
```



