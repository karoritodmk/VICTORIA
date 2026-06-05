# VICTORIA
 aplicativo informático que permita administrar, publicar y calificar guías y materiales del SENA en un solo lugar, asegurando que tanto instructores como aprendices gestionen sus portafolios de forma organizada y bajo las mismas reglas.

un aplicativo informático que permite administrar, publicar y calificar guías y materiales del SENA en un solo lugar, asegurando que tanto instructores como aprendices gestionen sus portafolios de forma organizada y bajo las mismas reglas.

Proyecto VICTORIA: Sistema de Repositorio Pedagógico Integral VICTORIA es una plataforma de software diseñada específicamente para el entorno académico del SENA. Actúa como un repositorio centralizado y un sistema de gestión educativa que conecta la administración de contenidos con el flujo de evaluación.

-Objetivo Principal Proveer una solución tecnológica escalable que elimine la dispersión de documentos, permitiendo centralizar la administración, distribución y resguardo de materiales pedagógicos (como las guías de aprendizaje). A su vez, busca optimizar el flujo de trabajo de los instructores, estandarizando los procesos de evaluación y calificación mediante un entorno digital ágil.

Funcionalidades y Procesos Clave El sistema se divide en procesos específicos orientados a cubrir las necesidades tanto del almacenamiento como de la interacción académica:

Gestión y Publicación de Contenidos: Proceso de carga y catalogación de guías de aprendizaje y materiales didácticos. Validación estricta de la información de entrada mediante Pydantic antes de ser procesada por el servidor, asegurando la integridad de los datos. Módulo de Evaluación y Calificación: Herramientas dedicadas para cuentas con roles específicos (como la cuenta instructorsena53), permitiendo revisar entregas, realizar seguimiento y calificaciones emitidas directamente en la plataforma. Gestión de Base de Datos Relacional: Almacenamiento estructurado de usuarios, materiales y calificaciones utilizando PostgreSQL. Mapeo y consultas seguras a través de SQLAlchemy, garantizando que las relaciones entre instructores, aprendices y documentos se mantengan consistentes.

-Enfoque de Desarrollo y Arquitectura El desarrollo de VICTORIA se plantea bajo una arquitectura moderna y estructurada, garantizando que el sistema pueda crecer y mantenerse a largo plazo:

-Backend de Alto Rendimiento: Construido sobre Python y FastAPI, lo que garantiza respuestas rápidas y la creación de una API robusta para la comunicación de datos. Patrones de Diseño de Software: Para resolver problemas complejos de estructura y flujo de datos, el desarrollo integra patrones de diseño como Adapter (para compatibilizar diferentes interfaces o fuentes de datos) y Chain of Responsibility (para delegar la lógica de procesamiento y validación de peticiones de manera secuencial).

-Flujo UI/UX Iterativo: El desarrollo visual comienza con la creación de wireframes y prototipos en Figma (respetando la identidad visual, como el característico verde del logo del SENA). Posteriormente, estas interfaces se maquetan utilizando HTML5, CSS3 y Bootstrap, construyendo formularios web estéticos y completamente responsivos.

///el stack tecnológico actual///

-Backend y Lógica de Negocio Lenguaje principal: Python Framework API: FastAPI (para la creación de servicios web ágiles y de alto rendimiento) Validación de datos: Pydantic (control de esquemas y reglas de negocio) Patrones de diseño: Implementación de patrones estructurales y de comportamiento como Adapter y Chain of Responsibility.

Base de Datos y Persistencia Motor de base de datos: PostgreSQL ORM (Mapeo Objeto-Relacional): SQLAlchemy (para la gestión y mapeo de las tablas relacionales) Herramientas de soporte local: XAMPP y MySQL Workbench (utilizados para la administración de servicios y conexiones en el entorno local)

Frontend y Diseño UI/UX Prototipado y maquetación: Figma (diseño de wireframes e interfaces de usuario) Estructura y estilos base: HTML5 y CSS3 Famework CSS: Bootstrap (para el diseño responsivo de formularios y componentes de la interfaz)

Herramientas de Desarrollo y Entorno Editor de código: Visual Studio Code (VS Code)

Gestión de entornos virtuales: Herramientas nativas de Python (venv) combinadas con PowerShell para la activación y ejecución de scripts.

///cómo ejecutar el código Python ///

Paso 1: Abrir el proyecto en Visual Studio Code Abre Visual Studio Code. Selecciona Archivo > Abrir carpeta (Archivo > Abrir carpeta) y elige la carpeta de tu proyecto victoria. Abre una nueva terminal integrada dentro de VS Code (Ctrl + Ñ o Terminal > Nueva Terminal).

Paso 2: Activar el Entorno Virtual (Python venv) Como estamos utilizando un entorno virtual para aislar las dependencias y configuramos previamente la directiva de seguridad en PowerShell para evitar el error PSSecurityException, ejecuta el comando según tu sistema operativo en la terminal:

En Windows (PowerShell / CMD):

PowerShell .\venv\Scripts\activate (Sabrás que funcionó porque verás (venv) al inicio de la línea de comandos en tu terminal).

En macOS / Linux:

Bash source venv/bin/activate Paso 3: Asegurar las Dependencias Instaladas Para verificar que tienes FastAPI, SQLAlchemy, Pydantic y el conector de PostgreSQL listos, ejecuta:

Bash pip install -r requisitos.txt (Si ya están instalados, la terminal te indicará que ya se cumplen los requisitos).

Paso 4: Levantar la Base de Datos (PostgreSQL) Antes de iniciar el código Python, asegúrese de que su servicio de base de datos esté activo: Inicia su servidor local de PostgreSQL (comprobando su estado en sus herramientas de administración local). Verifique que las variables de entorno o la cadena de conexión en su código reflejen correctamente su DB_USER y contraseña para que SQLAlchemy pueda conectarse sin problemas de autenticación.

Paso 5: Ejecutar el Servidor de FastAPI con Uvicorn Con el entorno activo y la base de datos corriendo, inicia el servidor de desarrollo ejecutando el siguiente comando en la terminal:

Bash uvicorn main:app --reload ¿Cómo verificar que todo está corriendo bien? Una vez que ejecute el comando anterior, la terminal mostrará unas líneas de texto indicando que el servidor está encendido. Podrás acceder a la aplicación desde tu navegador a través de estas direcciones:

Aplicación principal: http://127.0.0.1:8000

Documentación interactiva de la API (Swagger UI): http://127.0.0.1:8000/docs (Aquí podrás probar directamente las rutas y validaciones de Pydantic que tiene el proyecto).

/// cómo visualizar los prototipos HTML///

Con el servidor corriendo, el navegador web cargará el HTML junto con todos sus estilos CSS y Bootstrap de forma automática. No utiliza extensiones como Live Server. Abre tu navegador e ingresa a:

Para interactuar con el sistema (Dashboard / Formularios con diseño completo): Ingresa a: http://127.0.0.1:8000/dashboard (o la ruta específica que configura el backend para la vista).

Para revisar y probar las rutas de la API (Swagger UI): Ingresa a: http://127.0.0.1:8000/docs
