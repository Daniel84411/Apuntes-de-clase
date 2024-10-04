# Metodo algebraico
Consisten en plantear ecuaciones algebraicas para asi poder obtener el comportamiento de un sistema el cual puede sea en el tiempo continuo o discreto como se ve en la siguiente figura

![Figura de prueba](Sistema.png)

$$Figura 1: Figura Sistema$$

## Metodo por igualacion de modelo
Para poder realizar este metodo hay que tener en cuenta los siguientes aspectos: Conocer la funcion en lazo abierto G(Z) y el comportamiento del sistema en lazo cerrado Go(z), mediante lo cual obtenemos la siguiente ecuacion que corresponde a la funcion del controlador C(z) para el correpondiente comportamiento.

$$C\left( Z \right)=\frac{Go\left( Z \right)}{G\left( Z \right) -Go\left( Z \right)*G\left( Z \right)}=\frac{Go\left( Z \right)}{G\left( Z \right)(1-Go\left( Z \right))}$$

*Hay que tener en cuenta que este metodo solo sirve para funciones causales o estrictamente propias por lo contrario se generaria un controlador no realizable

## Ejemplos 

💡**Ejemplo 1:**  Diseñar un controlador que tiene las siguientes funciones para G(Z) y Go(Z)

$$G\left( Z \right)=\frac{0,58}{Z^{2}-12,4Z+0,25} $$ 

$$Go\left( Z \right)=\frac{0,21Z+2}{Z^{2}-32,8Z+3,2}$$

Remplazamoss C(Z) haciendo uso del metodo expliado anteriormente para obtener el controlador

$$C\left( Z \right)=\frac{\frac{0,21Z+2}{Z^{2}-32,8Z+3,2}}{\frac{0,58}{Z^{2}-12,4Z+0,25}(1 - \frac{0,21Z+2}{Z^{2}-32,8Z+3,2})}$$

