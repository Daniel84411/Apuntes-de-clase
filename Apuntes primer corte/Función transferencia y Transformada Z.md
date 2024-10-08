# Transformada Z de adelantos y atrasos
## 1. Muestreo en términos matemáticos:
* Si se tiene una función 𝑓(𝑡) continua y se quiere expresar <br> matemáticamente el equivalente discreto:<br>
$$𝑦(𝑡)= 5𝑆𝑒𝑛(1.04𝑡)$$<br>
![](Imagenes/FuncionSeno.PNG)<br>
**Figura 1**<br>
$$T=0.5 seg$$<br>
![](Imagenes/FuncionDiscretaSeno.PNG)<br>
**Figura 2**

```
%% codigo de matlab Figura 1
t=0:(pi/100):9;
y= 5*sin(1.04*t);
plot(t,y)
%% codigo de matlab Figura 2
T=0:0.5:9;
y1= 5*sin(1.04*T);
stem(T,y1)
```
## 2. Función en términos de muestras
$$𝑓(𝑡)= 𝑓(𝑘𝑇)$$<br>
* T es el periodo de muestreo<br>
$$𝑦(𝑘𝑇) = 5𝑆𝑒𝑛 1,04𝑘𝑇 ; 𝑇 = 0.5 𝑠𝑒𝑔$$<br>
![](Imagenes/FuncionDiscretaSeno.PNG)<br>
$$𝑦(𝑘𝑇) = 5𝑆𝑒𝑛 1,04𝑘𝑇 ; 𝑇 = 0.2 𝑠𝑒g$$<br>
![](Imagenes/FuncionDiscreta2.PNG)<br>
**Figura 3**
```
T=0:0.2:9;
y1= 5*sin(1.04*T);
stem(T,y1)
```
# Representación matemática de los sistemas
## 1. Ecuación en diferencias
$$𝑏_𝑛𝑢(𝑘) + 𝑏_{𝑛-1}𝑢(𝑘−1)+ ⋯ + 𝑏_0𝑢(𝑘−𝑛) = 𝑦(𝑘)+𝑎_{𝑛−1}𝑦(𝑘 − 1)+ ⋯ + 𝑎_0𝑦(𝑘 − 𝑛)$$
* Donde “u” es la entrada y “y” es la salida
* La dinámica del sistema se representa a través de una combinación lineal de diferentes muestras de las señales
* Al igual que con las ecuaciones diferenciales, las ecuaciones en diferencias representan el comportamiento dinámico de un sistema en términos de sus señales de entrada y salida
## 2. Características ecuaciones en diferencias
* Las ecuaciones en diferencias pueden ser homogeneas, lineales, invariantes en el tiempo<br>
💡**Ejemplo 1:**
* $$𝑦(𝑘+3) + 0.08𝑦(𝑘+2) + 0.09𝑦(𝑘)𝑢(𝑘)= 0$$
  *  Lineal, invariante en el tiempo, no homogénea<br>
💡**Ejemplo 2:**
* $$𝑦(𝑘+2)+𝑠𝑒𝑛(0,7𝑘)𝑦(𝑘+3)+0,6𝑦(𝑘) = 0$$ 
  *  Lineal, variante en el tiempo, homogénea<br>
💡**Ejemplo 3:**
* $$𝑦(𝑘+1) = −0,04(𝑦(𝑘))^2$$
  *  No lineal, invariante en el tiempo, homogénea
## 3. Solución de ecuaciones en diferencias
* Las ecuaciones en diferencias se solucionan por dos enfoques fundamentales:
 * Métodos iterativos
   >🔑 *Definición:* Un método iterativo es un método que progresivamente va calculando aproximaciones a la solución de un problema
 * Transformada Z
   >🔑 *Definición:* Es una herramienta matemática que nos permite convertir una señal de tiempo discreto, que es una secuencia de números reales o complejos, en una representación compleja en el dominio de la frecuencia.
## 4. Solución por métodos iterativos
💡**Ejemplo 1:**<br>
$$𝑦(𝑘)=\frac{1}{4}(−3y(k−2)+y(k−3)+4u(k−5)−6u(k−8))$$
* Condiciones iniciales:<br>
  $$𝑦(−2) = 1; 𝑦(−3)= −2 ; 𝑢(𝑘)=2 \text{ si } 𝑘 = 0,1,2, … \text{ y } 𝑢(𝑘)=0 \text{ si } 𝑘 < 0$$<br>
* K=0
$$𝑦(𝑘)=\frac{1}{4}(−3y(−2)+y(−3)+4u(−5)−6u(−8))= - \frac{5}{4}$$
# Transformada Z
Es la contraparte discreta de la transformada de LaPlace
* El espacio z tiene características diferentes al espacio de LaPlace<br>
![](Imagenes/TransformadadeLaplaceyTransformadaZ.PNG)
## 1. Solución de ecuaciones en diferencias por transformada Z
* Es un procedimiento similar a la solución de ecuaciones diferenciales
 * Aplicar transformada Z a la ecuación
 *  Despejar la variable desconocida o salida del Sistema
 *  Aplicar transformada Z inversa $$𝑍^{−1}$$
## 2. Transfomadas Z importantes en control
* En las ecuaciones en diferencias tenemos términos del tipo:
* Donde n es el número de muestra que se desplaza la función <br>
$$𝑓(𝑘+𝑛) \text{ o } 𝑓(𝑘−n)$$<br>
* Entonces la transformada Z de este tipo de términos son muy importantes en el área de control
## 3. Atrasos
## 4. Transformada Z de un atraso
## 5. Adelantos
## 6. Transformada Z de un adelanto
# Función de transferencia discreta
## 1. Funciones de transferencia en el dominio Z
## 2. Función de transferencia pulso
## 3. Para dos sistemas en cascada
## 4. Lazo cerrado
## 5. Función de transferencia resultante
## 5. Pasar de una función de transferencia en atraso a adelanto
## 6. Sistemas no causales
## 7. Sistemas causales
## 8. Tiempo muerto en sistemas discretos



