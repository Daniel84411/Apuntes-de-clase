# Transformada Z de adelantos y atrasos
## Muestreo en términos matemáticos:
* Si se tiene una función 𝑓(𝑡) continua y se quiere expresar <br> matemáticamente el equivalente discreto:<br>
$$𝑦(𝑡)= 5𝑆𝑒𝑛(1.04𝑡)$$<br>
![](Imagenes/FuncionSeno.PNG)<br>
**Figura 1**<br> $$T=0.5 seg$$<br>
![](Imagenes/FuncionDiscretaSeno.PNG)<br>
**Figura 2**

```
%% codigo de matlab Figura 1
t=0:(pi/100):9;
y= 5*sin(1.04*t);
plot(t,y)
%% codigo de matlab Figura 2
n=linspace(0,9,length(y_n));
y_n=[0 2.5 4.5 5 4.5 2.5 0 -2.5 -4.5 -5 -4.5 -2.5 0 2.5 4.5 5 4.5 2.5 ];
stem(n,y_n,"LineWidth",0.5);
axis([0 9 -5 5]);
```

