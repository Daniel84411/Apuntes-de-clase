# El análisis en frecuencia y los diagramas de Bode
El análisis en frecuencia y los diagramas de Bode son herramientas fundamentales en la teoría de control y la electrónica para analizar y diseñar sistemas de control y filtros.
## Análisis en frecuencia
El análisis en frecuencia se enfoca en estudiar la respuesta de un sistema a señales de frecuencia variable. Se utiliza para evaluar la estabilidad, el comportamiento y el desempeño de un sistema en diferentes frecuencias.
* Un enfoque para analizar los sistemas dinámicos es
verificar su comportamiento en la salida a partir de
cambios en frecuencia en la entrada
* Se realiza aplicando señales seno $$𝑅 = 𝐴𝑠𝑒𝑛(𝜔𝑘𝑇 + 𝜃)$$
suponiendo que el sistema tiene un comportamiento
lineal
* Al realizar variaciones en la frecuencia de entrada se
producen variaciones en amplitud y fase en la señal de
salida
### Que cambia?
* Salida sinusoidal con amplitud proporcional
* Armónicos igual frecuencia que a la entrada
* Variaciones en amplitud y frecuencia
![](https://github.com/Daniel84411/Apuntes-de-clase/blob/ceddff9e8dbb3a461c9d3395e02a5bd64f4e3574/Imagenes/Planta.PNG)<br>
Figura 1: sistema.
## Representación matemática
Las señales sinusoidales son convenientes porque se
pueden representar en forma de fasores
* Los fasores asumen una frecuencia constante y
solamente representa la señal en términos de amplitud y
fase
* Si la entrada y salida se representan como fasores, el
sistema también es posible representarlo así.<br>
$$𝑅(𝑡) = 𝐴𝑆𝑒𝑛(𝜔𝑘𝑇 + 𝜑)$$<br>
$$R=𝐴∠𝜑$$
## Sistema en fasores
![](https://github.com/Daniel84411/Apuntes-de-clase/blob/eec28926a4d8ff87707c6310e097caf37f8daf97/Imagenes/Planta2.PNG)<br>
Figura 2: fasores del sistema<br>
$𝐺(𝑠)=\frac{𝐴_2∠𝜑_2}{𝐴_1∠𝜑_1}=M∠𝜑$<br>
Entonces M y 𝜑 son:<br>
$M=\frac{A_2}{A_1}$ y $𝜑=𝜑_2-𝜑_1$
## Expresar función de transferencia en términos de la frecuencia
* Se sabe de los sistemas continuos que:<br>
$$𝑠 = 𝑗𝜔$$<br>
* Y también que la equivalencia de mapeo de polos y zeros es:<br>
$$𝑧 = 𝑒^{𝑠T}$$<br>
* Por lo tanto para poner la variable z en términos de la frecuencia se obtendría:<br>
$$𝑧 = 𝑒^{𝑗𝜔T}$$<br>
💡**Ejemplo 1:**<br>
* Se tiene la función de transferencia con tiempo de muestreo 0.2 seg:<br>
  $$H(z)=\frac{1}{(z-0.2)(z-3)}$$<br>
* Se expresaría en el dominio de la frecuencia<br>
$$H(𝑗𝜔T)=\frac{1}{(𝑒^{𝑗𝜔T}-0.2)(𝑒^{𝑗𝜔T}-3)}$$<br>
$$H(𝑗𝜔T)=\frac{1}{(cos(𝜔T)+jsen(𝜔T)-0.2)(cos(𝜔T)+jsen(𝜔T)-3)}$$<br>
$$H(𝑗𝜔T)=\frac{1}{cos^{2}(𝜔T)-sen^{2}(𝜔T)-3.2cos(𝜔T)+0.6+j2cos(𝜔T)sen(𝜔T)-3.2jsen(𝜔T)}$$
## Diagramas de Frecuencia
* Para cualquier función de transferencia se puede separar la parte real e imaginaria, entonces es posible hallar la magnitud y la fase en el domino de la frecuencia
* Por lo tanto esto podría ser graficado en un plano para observar su comportamiento
  * Magnitud y Fase con respecto a la frecuencia
    * Escala lineal
    * Escala logarítmica Decibelios
  * Magnitud con respecto a la fase
    * Coordenadas Polares
## Diagramas de Bode
![](https://github.com/Daniel84411/Apuntes-de-clase/blob/10aa59277d383b7f086d4662242a2a0b89622c38/Imagenes/Diagrama-de-Bode.jpg)<br>
Figura 3: Diagrama de Bode<br>
Los decibelios dB no son una unidad física se utilizan como una interpolación de algunas cantidades como ganancia o potencia<br>
En el caso de la ganancia:<br>
$$𝐴_{𝑑𝐵}=20log_{10}A$$
## Análisis frecuencial en tiempo discreto
* No es posible hacer análisis en frecuencia directamente en tiempo discreto.
* Se aprovecha la transformación bilineal (Tustin) para aproximar al tiempo continuo:<br>
$$𝑤 =\frac{2}{𝑇}\frac{𝑧 − 1}{𝑧 + 1}$$<br><br>
$$z=\frac{(1+\frac{wT}{2})}{1-\frac{wT}{2}}$$<br>
* Reemplazando $$𝑧 = 𝑒^{𝑗𝜔𝑇}$$ se obtiene:<br>
$$𝑤 =j\frac{2}{𝑇}tan(\frac{𝜔𝑇}{2})$$<br>
* Sustituyendo $$w=jv$$ resulta:<br>
$$v=\frac{2}{𝑇}tan(\frac{𝜔𝑇}{2})$$<br>
![](https://github.com/Daniel84411/Apuntes-de-clase/blob/10aa59277d383b7f086d4662242a2a0b89622c38/Imagenes/An%C3%A1lisis%20frecuencial%20en%20tiempo%20discreto.PNG)<br>
Figura 4:Análisis frecuencial en tiempo discreto<br>
💡**Ejemplo 3:**<br>
* Si se tiene un sistema en tiempo continuo:<br>
$$G(s)=\frac{2}{s+11}$$
Se puede obtener la aproximación discreta (zoh)<br>
con $$T=0.3$$ seg:<br>
$$G(z)=\frac{2(1-e^{-11(0.3)})}{z-e^{-11(0.3)}}=\frac{1.9662}{z-0.03288}$$<br>
* Al aplicar la transformada w se obtiene:<br>
$$G(w)=\frac{1.9662}{(\frac{1+\frac{0.3w}{2}}{1-\frac{0.3w}{2}})-0.03288}$$<br>
$$G(w)=\frac{1.9662}{\frac{0.96712+0.15w(1+0.03288)}{1-0.15w}}$$<br><br>
$$G(w)=\frac{1.9662(1-0.15w)}{0.96712+0.15w(1+0.03288)}$$<br><br>
$$G(w)=\frac{1.9662(1-0.15w)}{0.96712+0.154932w}$$<br><br>
$$G(w)=\frac{12.688(−0.15w+1)}{w+6.243}$$
