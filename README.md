# LABORATORIO-5
# VARIABILIDAD DE LA FRECUENCIA CARDIACA (HRV) Y BALANCE AUTONOMICO
En esta practica vamos a analizar la variabilidad de la frecuencia cardíaca (HRV) como un indicador del balance entre la actividad simpática y parasimpática del sistema nervioso autónomo. Para ello, se adquirimos una señal ECG real en dos condiciones fisiológicas diferentes (reposo y lectura en voz alta), se procesa digitalmente mediante filtrado, detección de picos R y cálculo de intervalos R-R, y finalmente se estudia la HRV tanto en el dominio del tiempo como mediante el diagrama de Poincaré, permitiendo obtener índices cuantitativos de actividad simpática y vagal. La práctica integra conceptos de fisiología, adquisición de señales y procesamiento digital.

## objetivos 
- Identificar cambios en el balance autonómico mediante análisis temporal de la variabilidad de la frecuencia cardíaca (HRV).
- Analizar la variabilidad de la frecuencia cardíaca (HRV) como herramienta para evaluar el balance autonómico.
- Adquirir y procesar correctamente una señal ECG utilizando métodos de filtrado y detección de picos R.
- Comparar la respuesta autonómica del sujeto entre reposo y lectura en voz alta.
- Aplicar herramientas de análisis temporal y no lineal (diagrama de Poincaré) para caracterizar la HRV.
- Interpretar resultados fisiológicos relacionados con actividad simpática y parasimpática.

## PARTE A 
<img width="405" height="646" alt="image" src="https://github.com/user-attachments/assets/f09c40b5-a927-47cb-9919-5f8427ba733e" /><br>

## 𝘼𝙘𝙩𝙞𝙫𝙞𝙙𝙖𝙙 𝙎𝙞𝙢𝙥𝙖𝙩𝙞𝙘𝙖 𝙮 𝙋𝙖𝙧𝙖𝙨𝙞𝙢𝙥𝙖𝙩𝙞𝙘𝙖 𝙙𝙚𝙡 𝙨𝙞𝙨𝙩𝙚𝙢𝙖 𝙣𝙚𝙧𝙫𝙞𝙤𝙨𝙤 𝙖𝙪𝙩𝙤𝙣𝙤𝙢𝙤
El cuerpo humano mantiene un equilibrio constante entre los estados de actividad y reposo gracias al sistema nervioso autónomo, encargado de controlar funciones involuntarias como la respiración, el ritmo cardíaco y la digestión. Este sistema se divide en el sistema nervioso simpático y el sistema nervioso parasimpático, que trabajan de forma complementaria.<br>

El sistema nervioso simpático prepara al organismo para situaciones de alerta o estrés, aumentando la frecuencia cardíaca, dilatando las pupilas y proporcionando mayor energía al cuerpo. Por otro lado, el sistema nervioso parasimpático favorece los estados de descanso y recuperación, disminuyendo el ritmo cardíaco, estimulando la digestión y ayudando a conservar energía. Gracias a la acción coordinada de ambos sistemas, el cuerpo puede mantener su estabilidad y funcionamiento adecuado.<br>

<img width="800" height="800" alt="image" src="https://github.com/user-attachments/assets/c9beb138-d62a-4e0d-ae9f-431a2ba9a8e1" /><br>
El sistema nervioso simpático es el encargado de activar y acelerar las funciones del organismo, preparando al cuerpo para responder ante situaciones de peligro, estrés o emergencia. Se relaciona con la conocida respuesta de “lucha o huida”, ya que permite que la persona reaccione rápidamente frente a estímulos que requieren una acción inmediata.<br>

Cuando este sistema se activa, produce diferentes cambios fisiológicos en el cuerpo, como el aumento de la frecuencia cardíaca y respiratoria, la elevación de la presión arterial y la dilatación de las pupilas. Además, redistribuye el flujo sanguíneo, enviando mayor cantidad de sangre hacia el cerebro, el corazón y los músculos, mientras disminuye el aporte hacia órganos como el estómago y los intestinos. Gracias a estas respuestas, el organismo obtiene más energía y capacidad de reacción para enfrentar situaciones de alta demanda física o emocional.<br>

<img width="800" height="800" alt="image" src="https://github.com/user-attachments/assets/dfc248f6-e7c5-448b-860c-b896f02d7d25" /><br>
El sistema nervioso parasimpático es el encargado de promover el estado de relajación, descanso y recuperación del organismo después de situaciones de actividad o estrés. Su función principal es conservar y restaurar la energía del cuerpo, favoreciendo el mantenimiento de las funciones normales y el equilibrio interno del organismo.<br>

Cuando este sistema se activa, produce una disminución de la frecuencia cardíaca y respiratoria, reduce la presión arterial y favorece procesos como la digestión y la absorción de nutrientes. Además, estimula la actividad del estómago y los intestinos, permitiendo que el cuerpo entre en un estado de reposo y recuperación. Gracias a la acción del sistema nervioso parasimpático, el organismo puede recuperar energía, mantener la estabilidad de sus funciones vitales y favorecer el bienestar general.<br>


<img width="836" height="824" alt="image" src="https://github.com/user-attachments/assets/1489ae88-74ef-4197-9343-95989053f31b" /><br>
La actividad del sistema nervioso simpático y parasimpático tiene un efecto directo sobre la frecuencia cardíaca, ya que ambos regulan el funcionamiento del corazón de manera opuesta y complementaria.<br>

El sistema nervioso simpático aumenta la frecuencia cardíaca al preparar al organismo para situaciones de alerta, estrés o actividad física. Esto ocurre porque estimula al corazón para que lata más rápido y con mayor fuerza, permitiendo que llegue más sangre y oxígeno a los músculos y órganos que necesitan responder rápidamente.<br>

Por otro lado, el sistema nervioso parasimpático disminuye la frecuencia cardíaca, favoreciendo estados de reposo y recuperación. Su acción ayuda a que el corazón lata más lentamente, reduciendo el gasto de energía y permitiendo que el organismo mantenga un estado de calma y equilibrio.
Gracias a la interacción de ambos sistemas, el cuerpo puede adaptar la frecuencia cardíaca según las necesidades del momento, manteniendo un adecuado funcionamiento del organismo.<br>

<img width="836" height="824" alt="image" src="https://github.com/user-attachments/assets/859cbee5-8f78-42f2-8579-b164d3f8610d" /><br>
La variabilidad de la frecuencia cardíaca (HRV) es la variación en el tiempo que existe entre un latido cardíaco y el siguiente. Esta se obtiene a partir de la señal electrocardiográfica (ECG), mediante el análisis de los intervalos R-R, que corresponden al tiempo entre picos consecutivos de la onda R. La HRV es considerada un indicador importante del funcionamiento del sistema nervioso autónomo, ya que refleja el equilibrio entre la actividad simpática y parasimpática.<br>

Una HRV alta suele asociarse con un predominio de la actividad parasimpática, indicando un buen estado de adaptación, relajación y recuperación del organismo. En cambio, una HRV baja se relaciona con una mayor actividad simpática, asociada a situaciones de estrés, fatiga o sobrecarga física y emocional. Por esta razón, el análisis de la HRV es ampliamente utilizado en áreas clínicas, deportivas y de investigación para evaluar el estado cardiovascular y el nivel de estrés del cuerpo.<br>

<img width="836" height="824" alt="image" src="https://github.com/user-attachments/assets/cf72d28e-e603-431d-9506-bc6e0ebd1672" /><br>
El diagrama de Poincaré es una representación gráfica utilizada para analizar la variabilidad de la frecuencia cardíaca (HRV) a partir de la serie de intervalos R-R obtenidos del electrocardiograma (ECG). En este diagrama, cada intervalo R-R se grafica en función del intervalo siguiente, permitiendo observar de manera visual el comportamiento y la variabilidad de los latidos cardíacos.<br>

La forma y distribución de los puntos proporcionan información sobre el equilibrio del sistema nervioso autónomo. Una nube de puntos más amplia y alargada suele indicar una mayor variabilidad cardíaca y un predominio parasimpático, asociado a relajación y buena adaptación del organismo. Por el contrario, una distribución más compacta puede reflejar menor variabilidad y predominio simpático, relacionado con estrés o fatiga. Debido a esto, el diagrama de Poincaré es una herramienta útil para evaluar el estado cardiovascular y la regulación autónoma del corazón.<br>

## PARTE B 









## PARTE B

## PARTE C
