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
![](Imagenes/FuncionDiscretaSeno.PNG)<br>
**Figura 3**
```
T=0:0.2:9;
y1= 5*sin(1.04*T);
stem(T,y1)
```





