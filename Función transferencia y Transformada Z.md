# Transformada Z de adelantos y atrasos
## Muestreo en términos matemáticos:
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
## Función en términos de muestras
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
## Ecuación en diferencias
$$𝑏_𝑛𝑢(𝑘) + 𝑏_{𝑛-1}𝑢(𝑘−1)+ ⋯ + 𝑏_0𝑢(𝑘−𝑛) = 𝑦(𝑘)+𝑎_{𝑛−1}𝑦(𝑘 − 1)+ ⋯ + 𝑎_0𝑦(𝑘 − 𝑛)$$
* Donde “u” es la entrada y “y” es la salida
* La dinámica del sistema se representa a través de una combinación lineal de diferentes muestras de las señales
* Al igual que con las ecuaciones diferenciales, las ecuaciones en diferencias representan el comportamiento dinámico de un sistema en términos de sus señales de entrada y salida
## Características ecuaciones en diferencias
* Las ecuaciones en diferencias pueden ser homogeneas, lineales, invariantes en el tiempo
* 
 * Lineal, invariante en el tiempo, no homogénea
 *  
## Solución de ecuaciones en diferencias
## Solución por métodos iterativos
## Transformada Z
## Relación Z y L
## Solución de ecuaciones en diferencias por transformada Z
## Transfomadas Z importantes en control
## Atrasos
## Transformada Z de un atraso
## Adelantos
## Transformada Z de un adelanto
# Función de transferencia discreta



