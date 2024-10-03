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



