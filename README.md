# Proyecto_2_semestre_2023-1
# Revisión, rediseño e implementación de un robot móvil Rasbot UNAM

# Participantes
- Erik Peña Medina (responable).
- Rojas Trejo Sebastián (participante)
- Luis García Mejía (participante)
- Andrés David Flores Ferro (participante)

# Contenido
- [Objetivo](https://github.com/mrg-mex/Proyecto_02_semestre_2023-1/blob/main/README.md#objetivo)
- [Metas](https://github.com/mrg-mex/Proyecto_02_semestre_2023-1/blob/main/README.md#metas)
- [Productos](https://github.com/mrg-mex/Proyecto_02_semestre_2023-1/blob/main/README.md#productos)
- [Introducción](https://github.com/mrg-mex/Proyecto_02_semestre_2023-1/blob/main/README.md#introducci%C3%B3n)
- [Desarrollo](https://github.com/mrg-mex/Proyecto_02_semestre_2023-1/blob/main/README.md#desarrollo)
- [Conclusión](https://github.com/mrg-mex/Proyecto_02_semestre_2023-1/blob/main/README.md#conclusi%C3%B3n)

# Objetivo

Implementar un robot móvil (2,0) el cual podrá ser utilizado para la programación de algoritmos de navegación mediante el uso de sensores ultrasónicos y análisis de imágenes.

# Metas

- Evaluar y rediseñar el diseño del robot móvil con el fin de incorporar un par de sensores ultrasónicos y el driver de control de los motores. 
- Desarrollar de una simulación del robot móvil en el simulador Gazebo mediante su implementación en ROS2.
- Implementar los resultados de la simulación en un ambiente definido para los robots.

# Productos

- Un banco de pruebas virtual en el cual se pueden programar diferentes algoritmos de navegación en el robot móvil. 
- Un banco de pruebas físico en el cual puedan ser implementados los algoritmos comprobados en el banco de pruebas virtual.
- Un repositorio con todos los archivos generados durante el desarrollo del proyecto.

# Introducción
Un robot móvil es capaz de moverse autónomamente y de ejecutar determinadas acciones. Junto a la movilidad, por tanto, la independencia del robot respecto de la intervención humana es uno de los aspectos esenciales de la robótica móvil.
La robótica móvil actualmente aún se encuentra en un estadio relativamente temprano de su desarrollo, hace varios años que se utilizan prototipos y productos en serie en diferentes sectores como en el transporte, la agricultura, vehículos autónomos, etc.

Algunas de las características que presenta la robótica móvil son:
- Percepción mediante sistemas sensores
- Capacidad de adaptación ante circunstancias espaciales modificadas
- Navegación, planificación y actuación autónomas
- Software/programación orientados a tareas 

Por medio de este documento se intenta plasmar algunas situaciones de diseños que se solucionaron en el robot raspbot como lo es el redimensionamiento de algunas piezas, la corrección de problemas al abrir archivos en solidworks, el diseño y ensamble de nuevas piezas, entre otras actividades que se especificaran en el documento.
Lo anterior se planteó solucionar mediante la separación de actividades usando issues y mediante el uso del programa solidworks y finalmente los resultados obtenidos se encuentran descritos a lo largo de documento.



# Desarrollo

Las problemáticas del robot móvil (2,0) comenzaron con la presencia de errores en los archivos Chasis_2-1 y Chaster_shorun_65-1 provenientes del ensamble CAD, siendo la pieza de chasis del robot y la pieza del sistema de rueda bola loca respectivamente. Por lo tanto este fue el primer problema que se atacó y por ende el primero que se resolvió, siendo de vital importancia para el correcto desarrollo del proyecto debido a que bajo éste ensamble y sus archivos, trabajaría todo el equipo.

Al tener un ensamble libre de errores, procedimos a identificar, estructurar, organizar y delimitar tareas por medio de problemáticas o issues usando GitHub como herramienta. Identificamos y propusimos en total seis problemas principales en cuanto a diseño se refiere:

- Actividad 1: Arreglar archivos actuales que originan errores de ensamble.
- Actividad 2: Diseño colocación del sistema de sensores ultrasónicos.
- Actividad 3: Cambio diseño superior de robot móvil, NUEVO Ventilador para Raspberry.
- Actividad 4: Modificaciones en chasis para problemáticas actuales.
- Actividad 5: Detalles para base superior código QR.
- Actividad 6: Recuperar diseño actual de pieza. Rueda bola loca.

En base a estas problemáticas y con la primera de ellas ya resuelta (arreglo de archivos) distribuimos las problemáticas entre los tres integrantes de este proyecto para así, lograr un mayor avance en la solución y conclusión de la lista de problemas; sin dejar de lado una comunicación entre los integrantes del equipo ante cualquier situación o solicitud de apoyo.

Para iniciar nuestras respectivas actividades, lo primero que se hizo fue analizar el robot móvil físicamente para anotar dimensiones, observar los elementos que los componen y su distribución, ver los espacios o secciones no aprovechadas en el chasis y su factibilidad de realizar modificaciones en ese espacio específico. Esto nos brindó mucha información en nuestra lluvia de ideas para lograr la solución más creativa y óptima. Asimismo, aprovechamos para tomar las medidas correctas principalmente de la rueda bola loca, siendo un proceso esencial en la actividad 6 para comparar las medidas reales con las medidas establecidas en el CAD y modificarlas a su valor real. De manera secundaria, se observó y midió el ventilador para la Raspberry con fines de lograr una eficaz modificación en la parte superior del robot. Finalmente pero no menos importante, se observó el modelo para obtener ideas acerca de la colocación de tres sensores ultrasónicos y el doble puente H que llevará el robot para el control de los dos motores CD.

Las modificaciones al chasis del robot móvil fueron una parte vital de nuestro proyecto, ya que ésta actividad tenía relación con la base superior, las conexiones con el microprocesador Raspberry y el doble puente H y la colocación de los sensores ultrasónicos, por ende, las primeras modificación que se hicieron fueron en beneficio de la óptima conexión entre la Raspberry y el doble puente H, y modificaciones para la colocación de la base superior.

Para la base superior, se modificaron los diámetros de los orificios donde se insertan los postes de latón que sujetan a la Raspberry y se extruyeron un par de milímnetros más para aumentar la altura de la base y así liberar la entrada micro SD. Para garantizar que el usuario que maneje el robot móvil no tenga problemas con la inserción y retiro de la micro SD, los orificios se separaron ligeramente de la base para la cámara.

Las siguientes modificaciones a trabajar fueron los elementos para la conexión del microcontrolador y el puente H. Dicha conexión se logró perforando en forma de ranura el lateral del chasis para que, de esta manera los cables que deriven de la Raspberry puedan pasar por esta ranura y no dificulte el desplazamiento del robot. Para la colocación del doble puente H se realizó una serie de canales o correderas, en donde se deslizará y sujetará el módulo con los pines disponibles para conexión. Como complemento, se realizó un arco en el lateral del chasis, cerca de la ranura con el fin de que por ahí pasen los cables de conexión y se contengan dentro del arco, evitando que los cables sobresalgan demasiado y estorben en su funcionamiento más de lo que ayudan.

![image](https://user-images.githubusercontent.com/42391642/212604274-cc207020-5077-4566-97f3-69bce967d1d6.png)
![image](https://user-images.githubusercontent.com/42391642/212604324-6934ea45-07c8-4d9e-b677-515ee8c0f8b4.png)

La última modificación para el chasis dependía del diseño previo realizado para la colocación de los tres sensores ultrasónicos. Se llegó a un primer modelo, el cual, después de ser analizado y ensamblado a la estructura, se desechó debido al sesgo y posibles errores de sensado debido a la distribución propuesta.

![image](https://user-images.githubusercontent.com/42391642/212604683-fe5890d1-6e33-4c1e-bb5c-2108b7dcf41e.png)

Procedimos a realizar una segunda propuesta, donde dos de los sensores ultrasónicos estarán en la parte superior del chasis a los laterales y el tercero se encontrará enfrente de éste, en la parte inferior, haciendo analogía a una defensa de auto. La estructura para la colocación de los dos sensores laterales estará integradas directamente al chasis, mientras que el tercero se montará con ayuda de una pieza externa. Con estos requerimientos y consideraciones, procedimos a modificar el chasis con las operaciones oportunas para lograr el correcto ensamble y montaje de los tres sensores, solucionando así la actividad 2 y 4

![image](https://user-images.githubusercontent.com/42391642/212605092-e890cfb2-9766-4a88-b0b4-de7fb43a52a3.png)

Para la solución de la actividad 3 (el ventilador), se encontró un CAD existente con las dimensiones requeridas, se colocó en el CAD e implementaron restricciones para mantenerlo en el lugar adecuado dentro del archivo de ensamble y finalmente se modificó la base para lograr una disminución de espacio.

![image](https://user-images.githubusercontent.com/42391642/212605892-d9da0a0b-eb94-4a3a-a07d-c84604dd0a06.png)

La actividad 5, al estar relacionada de igual manera con la base (la cual fue modificada en la actividad 3), logró solucionarse de una manera más sencilla con el acomodo del ventilador y la base del código QR.

![image](https://user-images.githubusercontent.com/42391642/212606318-d1f9dedf-eb36-421d-8e6d-9f46f7a7fd30.png)

Para la actividad 6 bastó con modificar los elementos que componían la rueda bola loca y ajustarlos a las medidas reales realizadas en el laboratorio.

![image](https://user-images.githubusercontent.com/42391642/212606375-01f496ec-193f-48f4-8205-17df116cdbf6.png)

De esta forma se concluyeron exitosamente las actividades propuestas al inicio del proyecto, logrando obtener un archivo ensamble completo, que inmediatamente se mandó a imprimir para observar y probar los resultados finales de nuestro trabajo. Sin embargo, esto no fue posible debido a un problema con la boquilla en la impresora 3D, dificultando la salida del material para la fabricación el chasis. 

Finalmente se decidió que la mejor solución será cambiar la boquilla por una nueva y mandar el archivo nuevamente a impresión.

Se anexa una fotografía de la impresión resultante antes de que la impresora sufriera este percance.

![IMG_5589](https://user-images.githubusercontent.com/42391642/212607940-1cbf31d9-646b-418d-8706-08bab4f79812.JPG)
![IMG_5591](https://user-images.githubusercontent.com/42391642/212607959-23c397f9-b5a9-4b56-9d2e-9c984d4c3a75.JPG)

# Conclusión

