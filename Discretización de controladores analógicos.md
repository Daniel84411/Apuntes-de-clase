# Discretización de controladores Analógicos
El objetivo von estos es buscar una equivalencia entre los espacios de laplace y z,para lo cual existen diferentes metodos parab poder hallar esta relacion o equivalencia.
## Metodo de invarianza al impulso
### 1. Invarianza al impulso
Haciendo uso de la respuesta al impulso en el espacio de laplace para hallar su equivalente en z, en donde se debe asumir un tiempo de muestreo T con lo cual se obtienela siguiente ecuacion:

<a href="http://www.alciro.org/tools/matematicas/editor-ecuaciones.jsp?eq=C(z)=TZ\left\{ l^{-1}\left\{ C(s) \right\}_{t=KT} \right\}"><img src="http://www.alciro.org/cgi/tex.cgi?C(z)=TZ\left\{ l^{-1}\left\{ C(s) \right\}_{t=KT} \right\}" title="C(z)=TZ\left\{ l^{-1}\left\{ C(s) \right\}_{t=KT} \right\}" border="0" /></a>

💡**Ejemplo 1:** Teniendo en cuenta $C\left( s \right)=\frac{\frac{3}{7}}{\left( s + 3 \right)}+\frac{5}{\left( s + 7 \right)}$ hallar la solucion mediante el metodo anterior con un valor de T=2

<a href="http://www.alciro.org/tools/matematicas/editor-ecuaciones.jsp?eq=l^{-1}\left\{ C\left( s \right) \right\}"><img src="http://www.alciro.org/cgi/tex.cgi?l^{-1}\left\{ C\left( s \right) \right\}" title="l^{-1}\left\{ C\left( s \right) \right\}" border="0" /></a>   $$=\frac{3}{7}e^{-3t} + 5e^{-7t}$$ 
