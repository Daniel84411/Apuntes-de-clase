# Discretización de controladores Analógicos
El objetivo con esto es buscar una equivalencia entre los espacios de laplace y z,para lo cual existen diferentes metodos parab poder hallar esta relacion o equivalencia.
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

💡**Ejemplo 2:** Para  $C\left( s \right)=\frac{8}{\left( s + 9 \right)}+\frac{2.5}{\left( s + 2 \right)}$ hallar la solucion con T=0.3

$$l^{-1}\\{ C\left( s \right) \\}=8e^{-9t} + 2.5e^{-2t}$$ 

$$l^{-1}\\{ C\left( s \right) \\}_{t=KT}=8e^{-9KT} + 2.5e^{-2KT}$$ 

$$C\left( Z \right)=TZ\\{ 8e^{-9KT} + 2.5e^{-2KT} \\}$$

$$C\left( Z \right)=T\left[ 8\frac{z}{z-e^{-9T}} + 2.5\frac{z}{z-e^{-2T}} \right]$$

$$C\left( Z \right)=0.3\left[ 8\frac{z}{z-e^{-2.7}} + 2.5\frac{z}{z-e^{-0.6}} \right]$$

$$C\left( Z \right)=\frac{2.4z}{z-e^{-2.7}} + \frac{0.75z}{z-e^{-0.6}} $$

$$C\left( Z \right)=\frac{2.4z}{z-0.07} + \frac{0.75z}{z-0.5} $$

$$C\left( Z \right)=\frac{3.15z^{2}-1.25z}{z^{2}-0.57z+0.035}$$
### 2. Invarianza al paso
Tomando en cuenta la transformada z de un paso $Z\\{ e\left( t \right) \\}=\frac{z}{z-1}$ se puede hacer una igualdad entre las transofrmadas inversas de ambos espacios:

$$Z^{-1}\\{ C\left( z \right) \frac{z}{z-1} \\} = l^{-1}\\{ C\left( S \right) \frac{1}{s} \\}$$

Con lo cual haciendo remplazos obtenemos la ecuacion para C(z) que se muestra a continuacion:

$$C\left( z \right)=\frac{z}{z-1}Z\\{ l^{-1}\\{ C\left( s \right) \frac{1}{s} \\} \\}$$

### 3. Metodo Euler adelante
Esta tiene como base una aproximacion a la funcion discreta de una derivada tomando valores hacia adelante a la cual se le aplica la transformada z y se obtiene una equivalente entre el espacio de laplace y el espacio z

$$\frac{\mathrm{d} }{\mathrm{d} KT}x\left( KT \right)=\frac{x\left( k+1  \right)-x\left( k \right)}{T}$$

$$Z\\{ \frac{x\left( k+1  \right)-x\left( k \right)}{T} \\}=\frac{zX(z)-X(z)}{T}=\frac{z-1}{T}X(z)$$

$$s\approx \frac{z-1}{T} $$

### 4. Metodo Euler atrás
Un meto similar al anterior pero en este caso en lugar de tomar los adelantos toma los atrasos para hallar la derivada y la equivalencia entre los espacios

$$\frac{\mathrm{d} }{\mathrm{d} KT}x\left( KT \right)=\frac{x\left( k \right)-x\left( k-1  \right)}{T}$$

$$Z\\{ \frac{x\left( k \right)-x\left( k-1  \right)}{T} \\}=\frac{X(z)-z^{-1}X(z)}{T}=\frac{1-z^{-1}}{T}X(z)$$

$$s\approx \frac{1-z^{-1}}{T}=\frac{z-1}{Tz} $$

### 5. Metodo trapezoidal de "Tustin"
Tomando en cuenta los datos que se presentan en la figura 1 se obtiene la equivalencia para este tipo de metodo

![Metodo trapezoide](https://ghsalazar.github.io/assets/images/tustin-1.svg)

Figura 1. Grafica metodo trapezoide

Respecto a lo anterior se obtienen las siguientes formulas:

$$s=\frac{\frac{2}{T}\left( z-1 \right)}{z+1}$$

$$z=\frac{1+\frac{Ts}{2}}{1-\frac{Ts}{2}}$$
