# Estabilidad en sistemas discretos 
Partiendo de la base principal de lo que es un sistema estable en donde posee una salida limitada en consecuencia a una entrata tambien limitada se encuentran varias diferencias entre la estabilidad en sistemas. La principal diferencia va en cuanto al comportamiento de los polos y ceros de cada una en donde su ubicacion cambia siendo para el espacio z la frontera en forma de circulo (ver figura 1) en cambio como ya se habia manejado antes en laplace la frontera es el eje vertical (ver figira 1), lo cual hace que sus criterios para estabilidad sean distintos. 

![Estabilidad sistemas](https://i.ytimg.com/vi/sn13Faf7ALI/maxresdefault.jpg)
Figura 1. Estabilidad de los sistemas 

💡**Ejemplo 1:** hallar los polos del siguiente sistema y definir si es o no estable:

$$G\left( z \right)=\frac{9}{z^{2}+6.4z-2}$$

$$Z=0.29$$

$$Z=-6.69$$

El sistema es inestable debido a que uno de sus polos es mayor que 1

💡**Ejemplo 2:** hallar los polos del siguiente sistema y definir si es o no estable:

$$G\left( z \right)=\frac{9}{z^{2}-1.3z+0.4}$$

$$Z=0.8$$

$$Z=0.5$$

El sistema es estable debido a que todos sus polos son menores que 1

## Estabilidad BIBO
### Teste de Jury
Este test es utilizado para poder determinar si un sistema en el espacio z es estable o no para funciones que tienen la siguiente forma:

$$D\left( z \right)= a_{0}z^{n}+a_{1}z^{n-1}+....+a_{n-1}z+a_{n}$$

Para lo cual antes de pasar a ser evaluada deben cumplirmse primero las sigueintes condiciones, las cuales de no cumplirse el sistema seria inestable:

