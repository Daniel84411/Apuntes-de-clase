  # Ventajas diseño por diagrama de Bode

   * Se puede visualizar el error de estado estacionario.
   * Se da una respuesta temporal con el diagrama de bode.
   * Se mide los margenes directamente de la estabilidad en la frecuencia.
   * Se realiza el procedimiento de diseños iguales en el tiempo continuo, dando solucion a la transformada W.


#  Controladores por analisis en frecuencia

  ### Adelanto de fase: Aumenta el ancho de la banda del sistema lo cual permite que el sistema responda con mayor velocidad, dando asi una ganancia en alta frecuencia y esto puede afectarse por el ruido de este.

  #### Atraso de fase: Reduce la ganancia en frecuencias altas sin que se afecten las bajas. la velocidad reduce lo cual mantiene una afectacion con el ruido.

  ### Atraso - adelanto de fase: Se mejoran las margenes de estabilida, lo cual permite aumentar el ancho de banda y disminuir el error en estado estacionario evitando el ruido.

  # Control PID
#### Red de atraso - adelanto 

* Esta parte PD afecta la  frecuencia y aumenta el angulo de adelanto mejorando la estabilidad.
* PI esta parte toma accion como una red de atraso
* El PID se sintoniza por analisis en frecuencia, se toma enfoque en el dominio del tiempo.

  ### Margenes de fase y ganancia

  * Ganancia del lazo abierto tomando omo requerido el lazo cerrado sea inestable.ç
  * se mide en dB.
  * se toma la referrencia la fase de 180º
  * MG > 0 es positivo
  * MG < 0 es negativo

    ### Margen de fase 

  * Es el cambio en la fasse abierto, requerido para que el sistema en lazo cerrado sea inestable.
  * se hace la medicion en grados (º).
  * la ganancia unitaria (0dB) es la medida de referencia.
  * MP > -180 º positivo 
  * MP < -180 º negativo

# Consideraciones de margenes de estabilida 

### Cosideraciones 
* si MG y MP son positivos, el sistema es estable en lazo cerrado.
* el MG - MP deben ser grandes
* Si MG - MP son negativos o 0, este sistema es inestable en lazo cerrado


# ¿ De que parametros depende margen de fase ?
 Para un sistema continuo en lazo cerrado el margen de fase y el % overshoot estan relacionados.

  ### Procedimiento de diseño 

  * la planta analogica se discretiza para obtener un equivalente G(z)
  * Transformar G(z) a G(W)
  * graficar los diagramas de bode frente a la funcion 
    
