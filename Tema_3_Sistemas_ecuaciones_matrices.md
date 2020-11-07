# SISTEMAS DE ECUACIONES LINEALES Y MATRICES

## 1. MATRICES

### 1.1. NOCIONES GENERALES

En lo que sigue, nuestros escalares pertenecerán a un cuerpo $K$.

>Recuerda: un cuepo es un conjunto $K$ con dos operaciones internas, suma y producto, en la que todo elemento tiene inverso para el producto (Ejemplos: $\mathbb Q$, $\mathbb R$).

#### **1.1.1. Noción de matriz**
Una matriz de $m$ filas y $n$ columnas sobre $K$ es una tabla de elemntos de $K$,

$$\left(\begin{array}{cccc}a_{11}&a_{12}&\cdots&a_{1n}\\
a_{21}&a_{22}&\cdots&a_{2n}\\
\vdots & \vdots & \ddots & \vdots\\
a_{m1}&a_{m2}&\cdots&a_{mn}
\end{array}\right)$$

donde

- $a_{ij} \in K$.
- $a_{ij}$ es el elemento que está en la fila $i$ y columna $j$.

#### **1.1.2. Tipos y elementos de matrices**

- Matriz cuadrada: $m=n$.
- Diagonal principal: $a_{11}, a_{22}, \ldots, a_{mm}$. 
- Triangular superior:

$$\left(\begin{array}{cccc}a_{11}&a_{12}&\cdots&a_{1n}\\
0&a_{22}&\cdots&a_{2n}\\
\vdots & \vdots & \ddots & \vdots\\
0&0&\cdots&a_{mn}
\end{array}\right)$$

- Triangular inferior:

$$\left(\begin{array}{cccc}a_{11}&0&\cdots&0\\
a_{21}&a_{22}&\cdots&0\\
\vdots & \vdots & \ddots & \vdots\\
a_{m1}&a_{m2}&\cdots&a_{mn}
\end{array}\right)$$

- Diagonal:

$$\left(\begin{array}{cccc}a_{11}&0&\cdots&0\\
0&a_{22}&\cdots&0\\
\vdots & \vdots & \ddots & \vdots\\
0&0&\cdots&a_{mn}
\end{array}\right)$$

- Escalar:

$$\left(\begin{array}{cccc}k&0&\cdots&0\\
0&k&\cdots&0\\
\vdots & \vdots & \ddots & \vdots\\
0&0&\cdots&k
\end{array}\right)$$

- Identidad ($I_n$):

$$\left(\begin{array}{cccc}1&0&\cdots&0\\
0&1&\cdots&0\\
\vdots & \vdots & \ddots & \vdots\\
0&0&\cdots&1
\end{array}\right)$$

### 1.2. TRANSFORMACIONES ELEMENTALES. FORMA NORMAL DE HERMITE

- Pivote de la fila $i$: el primer elemento no nulo de la fila $i$.
- Pivote de la columna $j$: el primer elemento no nulo de la columna $j$.

#### **1.2.1. Matriz escalonada por filas**

- Todas las filas nulas están al final.
- El pivote de cada fila no nula está a la derecha del pivote de la fila anterior.
- El pivote de cada fila no nula vale $1$.

#### **1.2.2. Matriz escalonada reducida por filas**

Es una matriz escalonada por filas que cumple, además:

- Si en una columna hay un pivote (de una fila), todos los elementos de esa columna (menos el pivote), son cero.

#### **1.2.3. Matriz escalonada por columnas**

- Todas las columnas nulas están al final.
- El pivote de cada columna no nula está a la más abajo que el pivote de la columna anterior.
- El pivote de cada columna no nula vale $1$.

#### **1.2.4. Matriz escalonada reducida por filas**

Es una matriz escalonada por columnas que cumple, además:

- Si en una fila hay un pivote (de una columna), todos los elementos de esa fila (menos el pivote), son cero.

#### **1.2.5. Ejemplo**

![Ejemplo 1](./Ejemplo1.png)

#### **1.2.6. Transformaciones elementales por filas**

Dadas dos matrices $A,B \in \mathcal M_{m\times n}(K)$, decimos que $B$ se ha obtenido a partir de $A$ mediante una transformación elemental por filas de

- Tipo I, si $B$ es el resultado de intercambiar dos filas de $A$.

- Tipo II, si $B$ es el resultado de sustituir una fila de $A$ por esa misma fila multiplicada por un escalar.

- Tipo III, si $B$ es el resultado de sustituir una fila de $A$ por el resultado de sumar a esa fila otra fila multiplicada por un escalar.

#### **1.2.7. Transformaciones elementales por columnas**

Se definen de forma análoga.

#### **1.2.8. Matrices equivalentes por filas**

Dos matrices $A,B \in \mathcal M_{m\times n}(K)$ de dice que son equivalentes por filas, escrito $A \sim_f B$, si $B$ se puede obtener a partir de $A$ aplicándole una cantidad finite de transformaciones elementales por filas.

#### **1.2.9. Matrices equivalentes por columnas**

Se define de forma análoga.

#### **1.2.10. Forma normal de Hermite por filas**

Toda matriz $A \in \mathcal M_{m\times n}(K)$ es equivalente por filas a una **única matriz escalonada reducida por filas** $B$. Para ello, se sigue el siguiente proceso:

1. Intercambiamos las filas de forma que los pivotes de las filas queden escalonados.
2. Hacemos 1 el pivote de la primera fila. Hacemos ceros debajo del pivote de la primera fila.
3. Hacemos 1 el pivote de la segunda fila. Hacemos ceros debajo y encima del pivote de la segunda fila.
4. Repetimos sucesivamente.

#### **1.2.11. Ejemplo**

Encontrar la forma normal de Hermite por filas de la matriz de $\mathcal M_{3 \times 4}(\mathbb Z_5)$:

$$\left(\begin{array}{cccc}
2&3&1&4\\
3&1&3&0\\
2&2&0&1
\end{array}\right)$$

#### **1.2.12. Forma normal de Hermite por filas**

Toda matriz $A \in \mathcal M_{m\times n}(K)$ es equivalente por filas a una **única matriz escalonada reducida por columnas** $B$. Para ello, se sigue el siguiente proceso:

1. Intercambiamos las columnas de forma que los pivotes de las columnas queden escalonados.
2. Hacemos 1 el pivote de la primera columna. Hacemos ceros a la derecha de éste.
3. Hacemos 1 el pivote de la segunda columna. Hacemos ceros a la derecha y a la izquierda de éste.
4. Repetimos sucesivamente.

#### **1.2.13. Rango de una matriz**

El rango de una matriz $A \in \mathcal M_{m\times n}(K)$ es el número de filas no nulas de la matrix normal de Hermite.

### 2.3. OPERACIONES CON MATRICES

#### **2.3.1. Suma de matrices**

Dos matrices $A,B \in \mathcal M_{m\times n}(K)$ se suman componente a componente, es decir:

$$\left(\begin{array}{cccc}a_{11}&a_{12}&\cdots&a_{1n}\\
a_{21}&a_{22}&\cdots&a_{2n}\\
\vdots & \vdots & \ddots & \vdots\\
a_{m1}&a_{m2}&\cdots&a_{mn}
\end{array}\right)+
\left(\begin{array}{cccc}b_{11}&a_{12}&\cdots&b_{1n}\\
b_{21}&b_{22}&\cdots&b_{2n}\\
\vdots & \vdots & \ddots & \vdots\\
b_{m1}&b_{m2}&\cdots&ab_{mn}
\end{array}\right)=
\left(\begin{array}{cccc}a_{11}+b_{11}&a_{12}+b_{12}&\cdots&a_{1n}+b_{1n}\\
a_{21}+b_{21}&a_{22}+b_{22}&\cdots&a_{2n}+b_{2n}\\
\vdots & \vdots & \ddots & \vdots\\
a_{m1}+b_{m1}&a_{m2}+b_{m2}&\cdots&a_{mn}+b_{mn}
\end{array}\right)$$

>Observa que $A$ y $B$ tienen las mismas dimensiones.

#### **2.3.2. Producto de matrices**

El producto de dos matrices $A \in \mathcal M_{m\times n}$ y $B \in \mathcal M_{n \times l}$ es:

$$\left(\begin{array}{cccc}a_{11}&a_{12}&\cdots&a_{1n}\\
a_{21}&a_{22}&\cdots&a_{2n}\\
\vdots & \vdots & \ddots & \vdots\\
a_{m1}&a_{m2}&\cdots&a_{mn}
\end{array}\right) \cdot
\left(\begin{array}{cccc}b_{11}&a_{12}&\cdots&b_{1l}\\
b_{21}&b_{22}&\cdots&b_{2l}\\
\vdots & \vdots & \ddots & \vdots\\
b_{n1}&b_{n2}&\cdots&ab_{nl}
\end{array}\right)=
\left(\begin{array}{cccc}c_{11}&c_{12}&\cdots&c_{1n}\\
c_{21}&c_{22}&\cdots&c_{2n}\\
\vdots & \vdots & \ddots & \vdots\\
c_{m1}&c_{m2}&\cdots&c_{ml}
\end{array}\right)$$

donde $c_{ij}$ es el resultado de multiplicar la fila $i$ de $A$ por la columna $j$ de $B$. Esta multiplicación se realiza del siguiente modo:

$$(a_{i1},a_{i2},\cdots, a_{in}) \cdot \left(\begin{array}{c}b_{1j}\\ b_{2j}\\ \vdots \\ b_{nj}\end{array}\right)=a_{i1}b_{1j}+a_{i2}b_{2j}+\cdots+a_{in}b_{nj} $$

>Observa que el número de columnas de $A$ es igual al número de filas de $B$.

#### **2.3.3. Ejemplos**

1. Sumar las siguientes matrices sobre $\mathbb Z_7$:

![Suma matrices](./Suma_matrices.jpg)

2. Multiplicar las siguientes matrices sobre $\mathbb Z_5$:

![Producto matrices](./Producto_matrices.jpg)

#### **2.3.4. Propiedades de las operaciones**

El conjunto $\mathcal M_m(K)$ de matrices cuadradas $m \times m$ sobre el cuerpo $K$ es un **anillo**. Es decir

1. $\mathcal M_m(K)$ es un grupo abeliano con la suma.

![Commutativo](./Commutativo.jpg)

2. El producto de $\mathcal M_m(K)$ es asociativo y tiene elemento unidad.

![Divisores cero](./Divisores_cero.jpg)

3. El producto es distributivo respecto de la suma.

#### **2.3.5. Ejemplos**

1. Dadas $A, B \in \mathcal M_3(\mathbb Q)$, calcula $A \cdot B$ y $B \cdot A$.

2. Dadas $A,B \in \mathcal M_2(\mathbb Z_5)$, calcula $A \cdot B$ y $B \cdot A$.

#### **2.3.6. Más propiedades**

1. El producto no es en general conmutativo. 

2. Existen divisores de cero.

3. No toda matriz tiene inversa.

### 2.4. MATRIZ TRASPUESTA

#### **2.4.1. Matriz traspuesta**

La matriz traspuesta de una matriz $A \in \mathcal M_{m\times n}(K)$, denotada $A^t$, es la matriz que resulta de poner en las columnas las filas de $A$.

#### **2.4.2. Propiedades de la matriz traspuesta**

1. $(A+B)^t=A^t+B^t$.
2. $(a \cdot A)^t = a \cdot A^t$.
3. $(A^t)^t=A$.
4. $(A \cdot B)^t=B^t \cdot A^t$.

#### **2.4.3. Traspuesta y forma normal de Hermite**

La forma normal de Hermite por columnas de $A$ puede obtenerse del siguiente modo:

1. Calculamos la forma normal de Hermite por filas $H$ de $A^t$.

2. La forma normal de Hermite por columnas es $H^t$.

### 2.5. MATRICES REGULARES

#### **2.5.1. Matrices regulares**

Una matriz $A \in \mathcal M_n(K)$ se dice regular si tiene inversa para el producto, es decir, si existe una matriz $B$ tal que

$$A \cdot B = B \cdot A = I_n$$

#### **2.5.2. Propiedades**

1. La inversa de una matriz regular es única.
2. Una matriz puede tener inversas por la derecha, pero no tener inversa. Por ejemplo, la matriz sobre $\mathbb Z_2$,

$$\left(\begin{array}{ccc}
1&0&1\\
1&1&0
\end{array}\right)$$

tiene dos inversas por la derecha,

$$\left(\begin{array}{cc}
1&1\\
1&0\\
0&1
\end{array}\right) \quad 
\left(\begin{array}{cc}
0&0\\
0&1\\
1&0
\end{array}\right)$$

3. $(A^{-1})^{-1} = A$.
4. $(A \cdot B)^{-1}=B^{-1} \cdot A^{-1}$.

#### **2.5.3. Matrices y rango**

Una matriz $A \in \mathcal M_n(K)$ es regular si y solo si tiene rango $n$.

Además, la inversa de $A$ se obtiene aplicando a la matriz identidad las mismas transformaciones que le apliquemos a $A$ para obtener la forma normal de Hermite de $A$ por filas.

#### **2.5.4. Ejemplo**

Matriz inversa de la matriz sobre $\mathbb Z_7$,

$$\left(\begin{array}{cc}
2&5\\
3&6
\end{array}\right)$$