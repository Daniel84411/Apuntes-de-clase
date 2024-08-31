# Discretización de controladores Analógicos
El objetivo von estos es buscar una equivalencia entre los espacios de laplace y z,para lo cual existen diferentes metodos parab poder hallar esta relacion o equivalencia.
## Metodo de invarianza al impulso
### 1. Invarianza al impulso
Haciendo uso de la respuesta al impulso en el espacio de laplace para hallar su equivalente en z, en donde se debe asumir un tiempo de muestreo T con lo cual se obtienela siguiente ecuacion:

$$C(z)=TZ\\{ l^{-1}\\{ C(s) \\}_{t=KT} \\}$$

💡**Ejemplo 1:** Teniendo en cuenta $C\left( s \right)=\frac{\frac{3}{7}}{\left( s + 3 \right)}+\frac{5}{\left( s + 7 \right)}$ hallar la solucion mediante el metodo anterior con un valor de T=0.1

$$l^{-1}\\{ C\left( s \right) \\}=\frac{3}{7}e^{-3t} + 5e^{-7t}$$ 

$$l^{-1}\\{ C\left( s \right) \\}_{t=KT}=\frac{3}{7}e^{-3KT} + 5e^{-7KT}$$ 

$$C\left( Z \right)=TZ\\{ \frac{3}{7}e^{-3KT} + 5e^{-7KT} \\}$$

$$C\left( Z \right)=T\left[ \frac{3}{7}\frac{z}{z-e^{-3T}} + 5\frac{z}{z-e^{-7T}} \right]$$

$$C\left( Z \right)=0.1\left[ \frac{3}{7}\frac{z}{z-e^{-0.3}} + 5\frac{z}{z-e^{-0.7}} \right]$$

$$C\left( Z \right)=\frac{0.3}{7}\frac{z}{z-e^{-0.3}} + 0.5\frac{z}{z-e^{-0.7}} $$

$$C\left( Z \right)=\frac{0.04z}{z-0.7} + \frac{0.5z}{z-0.5} $$

$$C\left( Z \right)=\frac{0.54z^{2}-0.37z}{z^{2}-12z+0.35}$$

💡**Ejemplo 1:** Para  $C\left( s \right)=\frac{8}{\left( s + 9 \right)}+\frac{2.5}{\left( s + 2 \right)}$ hallar la solucion con T=0.3

$$l^{-1}\\{ C\left( s \right) \\}=\frac{3}{7}e^{-3t} + 5e^{-7t}$$ 

$$l^{-1}\\{ C\left( s \right) \\}_{t=KT}=\frac{3}{7}e^{-3KT} + 5e^{-7KT}$$ 

$$C\left( Z \right)=TZ\\{ \frac{3}{7}e^{-3KT} + 5e^{-7KT} \\}$$

$$C\left( Z \right)=T\left[ \frac{3}{7}\frac{z}{z-e^{-3T}} + 5\frac{z}{z-e^{-7T}} \right]$$

$$C\left( Z \right)=0.1\left[ \frac{3}{7}\frac{z}{z-e^{-0.3}} + 5\frac{z}{z-e^{-0.7}} \right]$$

$$C\left( Z \right)=\frac{0.3}{7}\frac{z}{z-e^{-0.3}} + 0.5\frac{z}{z-e^{-0.7}} $$

$$C\left( Z \right)=\frac{0.04z}{z-0.7} + \frac{0.5z}{z-0.5} $$

$$C\left( Z \right)=\frac{0.54z^{2}-0.37z}{z^{2}-12z+0.35}$$
