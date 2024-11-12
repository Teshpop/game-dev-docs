![image](../images/ShaderNaveImg.png)
# Introducción 
- ## Descripción 
	En clase, se nos asigno el desarrollo de un shader que se aplicaría en un modelo de nave espacial con el objetivo de hacer manipulación de transparencias en objetos además de implementarlo con conocimientos adquiridos anteriormente.  
- ## Herramientas
	- Unity
	- Shader Graph

# Proceso
- Metodologia
	Se trabajo de manera iterativa, realizando cambios y probándolos en tiempo real en Unity para así asegurar de que los efectos fueras visibles y funcionaran correctamente.
- ## Etapas
	- ### Base
		Este grupo de nodos esta diseñado para definir la parte visual de la nave y realizar las siguientes funciones:
		- **Asignación de normales**: Configuración de las normales para asegurar un correcto sombreado y luz en la superficie de la nave.
		- **Textura Principal**: Asignar la textura base que se aplicara a la nave, definiendo su apariencia general
		- **CubeMap**: Integrar un CubeMap que permite simular efectos de reflexión y proporcionar una mayor profundidad visual.
		- **Aplicación de efectos**: 
			- **Fresnel**: Implementa el efecto Fresnel para crear variación en la intensidad del brillo según el ángulo de visión.
			- **Emisivo**: Añade un efecto emisivo en áreas de la textura, permitiendo que ciertas partes de la nave brillen y se destaquen visualmente.
		![[Pasted image 20241029120147.png]]
	- ### Transición 
		- Este grupo de nodos se encarga de realizar la transición entre la vista base y una vista transparente, permitiendo una experiencia visual fluida y atractiva. Sus funciones son las siguientes.
		- **Textura de Transición:** Se utiliza una textura específica diseñada para crear el efecto de transición. Esta textura puede incluir variaciones de opacidad y patrones que se adaptan a la estética del proyecto, proporcionando un cambio visual atractivo entre los estados.
		- **Manipulación de Posición:** Ajusta la posición de la textura a lo largo del proceso de transición. Esto permite que la textura se desplace suavemente, creando un efecto visual de desvanecimiento que facilita la transición entre la vista base y la transparente. La manipulación de la posición se puede personalizar para lograr diferentes tipos de transiciones, como deslizamientos o giros.
		- **Efecto de Movimiento:** Además de la transición, se implementa un efecto de movimiento que añade dinamismo a la visualización. Este efecto puede incluir variaciones en la velocidad y dirección del movimiento, lo que ayuda a mantener la atención del espectador y a mejorar la inmersión en la experiencia visual. La combinación de la textura de transición y el movimiento crea un impacto visual que enriquece la presentación.
		![[Pasted image 20241029121028.png]]
	- ### Blur
		- Este grupo de nodos es responsable de implementar la transparencia y el efecto de desenfoque (blur) en el objeto. A continuación se detallan sus funciones principales:
		-  **Implementación de Transparencia:** Se utiliza la información del entorno para determinar el nivel de transparencia del objeto. Esto se logra tomando como referencia lo que se encuentra detrás del objeto, permitiendo que se vea a través de él. Este proceso asegura que la transparencia sea coherente con la escena circundante y mejora la integración del objeto en su entorno.
		-  **Captura del Color de la Escena:** Se toma varias muestras del color de la escena para crear un fondo dinámico. Estas muestras permiten separar los distintos elementos visuales, lo que es crucial para lograr un efecto de desenfoque realista. La combinación de estas muestras asegura que el desenfoque mantenga la coherencia con los colores y luces de la escena.
		- **Creación del Efecto de Blur:** Usando la información obtenida del color de la escena, el grupo de nodos aplica el efecto de desenfoque. Esto se logra mediante técnicas de mezcla y manipulación de los colores de fondo, lo que produce un desenfoque que da una sensación de profundidad y suavidad. El desenfoque se puede ajustar en función de la intensidad deseada, permitiendo variaciones que van desde un ligero desenfoque hasta un efecto más pronunciado.
		![[Pasted image 20241029121537.png]]
# Resultados
- **Desarrollo Visual de la Nave:**
    - Implementación de un grupo de shaders que asigna normales, texturas y CubeMap, permitiendo efectos visuales como el Fresnel y un efecto emisivo, lo que mejora la estética y realismo de la nave.
- **Transiciones Dinámicas:**
    - Creación de un grupo de nodos que facilita la transición entre la vista base y la vista transparente, utilizando texturas específicas y manipulando la posición para lograr efectos de movimiento atractivos.
- **Transparencia y Desenfoque:**
    - Implementación de un grupo de nodos para gestionar la transparencia y el efecto de desenfoque, utilizando referencias del entorno y capturando el color de la escena para crear un desenfoque dinámico que enriquece la visualización del objeto.
- **Experiencia Visual Mejorada:**
    - La combinación de estos efectos ha resultado en una experiencia visual más inmersiva, con transiciones suaves y elementos que interactúan de manera coherente con su entorno.
