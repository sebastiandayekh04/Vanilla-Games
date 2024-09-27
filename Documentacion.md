Escenario del proyecto
Vanilla Games S.L. es una empresa que desarrolla minijuegos para navegadores web utilizando exclusivamente vanillaJS (Javascript puro, sin frameworks). La empresa cuenta con 10 desarrolladores y suele tener 3 alumnos en prácticas, de los cuales uno tiene muchas posibilidades de integrarse en el equipo al finalizar su formación.

La empresa sigue un método de trabajo en el que cada miembro del equipo propone un minijuego, el cual es valorado por sus compañeros. Un equipo responsable selecciona los proyectos con mayor potencial para ser desarrollados por todo el equipo y comercializados posteriormente. Hasta ahora, usaban herramientas ofimáticas para gestionar comentarios y valoraciones, pero planean crear una aplicación web tipo intranet para facilitar este proceso.

Como alumno en prácticas, tu tarea será desarrollar una aplicación web que permita a los desarrolladores publicar sus propuestas de minijuegos y recibir comentarios y valoraciones del resto del equipo.

Requisitos del proyecto y casos de uso general
La aplicación debe permitir:

Registro e inicio de sesión: Los usuarios podrán registrarse (nombre, apellidos, email, contraseña) y luego iniciar/cerrar sesión.
Perfil de usuario: Los usuarios registrados podrán editar su perfil y subir un avatar.
Publicación de proyectos: Los desarrolladores podrán publicar proyectos con información como nombre, descripción, imagen, enlaces (servidor de pruebas y repositorio de código), estado del proyecto, etc. También podrán editar o eliminar sus proyectos.
Comentarios y valoraciones: Los desarrolladores podrán comentar y valorar los proyectos publicados.
Roles de usuario:
Desarrollador: Publicar proyectos, comentar y valorar.
Administrador: Gestionar perfiles de usuario, roles, comentarios y valoraciones.
Fases de desarrollo
1. Definición del proyecto y requisitos básicos
Clarificación de todas las funcionalidades de la aplicación teniendo en cuenta los roles de acceso.

2. Definición de las versiones
El desarrollo se dividirá en varias versiones operativas, donde cada una amplía funcionalidades.

3. Planificación del proyecto
Basado en la metodología Agile, dividiremos el proceso en tareas que se agruparán, temporizarán y representarán mediante diagramas.

4. Diseño de la interfaz (DCU)
Benchmarking: Analizar la competencia.
Modelo de usuarios.
Prototipos de bajo nivel (Wireframes).
Mockups y guía de estilos (Figma).
Pruebas de usabilidad y rediseño.
5. Programación del Frontend
Maquetación con HTML/CSS.
Lógica de validación con VanillaJS.
6. Programación del Backend
Backend con Supabase.
Base de datos relacional (PostgreSQL).
ORM en Javascript para acceder a la BD.
7. Integración Frontend y Backend
Programación de la SPA.
Integración del ORM y manejo de roles, sesiones, etc.
8. Análisis de Usabilidad II
Pruebas de usabilidad y resolución de conflictos.

9. Testing y despliegue en producción
Creación de tests unitarios.
Configuración de CI/CD.
Despliegue en producción.
Versiones
VERSIÓN 1.0: Implementación de la publicación de proyectos
VERSIÓN 2.0: Implementación de los comentarios de los proyectos
VERSIÓN 3.0: Implementación del sistema de valoración mediante estrellas
VERSIÓN 4.0: Implementación del sistema de valoración basado en rúbricas o criterios de valoración
Arquitectura y tecnologías
Arquitecturas
La aplicación utilizará Client-side Rendering (CSR), en donde el cliente renderiza el HTML y se conecta al backend para obtener los datos en formato JSON. Esto permite separar el frontend del backend y desarrollar de manera independiente.

Diseño del Frontend
Prototipos: Se crearán usando HTML5, CSS3, y Bootstrap 5. Adaptaremos el diseño con SASS.
SPA y lógica de programación: Se implementarán con VanillaJS (ES6).
Implementación del Backend
Supabase: Base de datos, autenticación, control de roles, almacenamiento de archivos, y API para peticiones CRUD.
Entorno de desarrollo: VSCODE
Usaremos VSCode configurado con plugins necesarios.
El código seguirá el estándar 'Standard' mediante Eslint.
Usaremos Git para el control de versiones, con un flujo de trabajo basado en ramas funcionales.
Despliegue
Para pruebas: GitHub Pages.
Para producción: Servicios como Railway o Netlify.

https://carrebola.github.io/vanillaPill/assets/images/image-11-de7ef12dc76ee6bfa5555269933be7cb.png



Casos de uso específicos y diagramas de flujo.
En el primer apartado 'Requisitos y diagrama de casos de uso' para esta versión 1.0, hemos definido de manera general los casos de uso que se contemplan para cada actor y los hemos reflejado en un diagrama de casos de uso.

Es el momento de ser más concretos y detenernos a reflexionar en cada uno de los procesos que se realizarán para cada tarea, incluyendo los posibles errores cometidos por el usuario o el propio sistema.

Casos de uso específicos
1. Registrar usuario
Actores: Usuario no registrado.

Precondiciones: El usuario no ha iniciado sesión.

Flujo básico:

El usuario navega a la página de registro.
El usuario introduce su nombre, apellidos, email y contraseña.
El sistema valida que los campos estén completos y que el email no esté registrado previamente.
El sistema crea un nuevo usuario con los datos proporcionados.
El sistema muestra un mensaje de confirmación y redirige al usuario a la página de inicio.
Flujos alternativos:

3a. El sistema detecta que el email ya está registrado: muestra un mensaje de error y no crea la cuenta.
2. Recuperar contraseña
Actores: Usuario registrado.

Precondiciones: El usuario no ha iniciado sesión.

Flujo básico:

El usuario navega a la página de registro.
El usuario selecciona la opción 'Recuperar contraseña'
El sistema valida que el campo 'email' esté completo y que el email esté registrado previamente.
El sistema muestra un mensaje de confirmación de envio del mail para la recuperación de contraseña y redirige al usuario a la página de inicio.
Flujos alternativos:

3a. El sistema detecta que el email no está registrado: muestra un mensaje de error y no envia el mail.
3. Iniciar sesión
Actores: Usuario registrado.

Precondiciones: El usuario no ha iniciado sesión.

Flujo básico:

El usuario navega a la página de inicio de sesión.
El usuario introduce su email y contraseña.
El sistema valida las credenciales y crea una sesión para el usuario.
El sistema redirige al usuario a la página principal de la aplicación.
Flujos alternativos:

3a. Las credenciales son incorrectas: el sistema muestra un mensaje de error y no crea la sesión.
4. Cerrar sesión
Actores: Usuario registrado.

Precondiciones: El usuario ha iniciado sesión.

Flujo básico:

El usuario hace clic en el botón de "cerrar sesión".
El sistema cierra la sesión del usuario.
El sistema redirige al usuario a la página de inicio.
4. Ver/Editar perfil
Actores: Usuario registrado.

Precondiciones: El usuario ha iniciado sesión.

Flujo básico:

El usuario navega a la página de edición de perfil.
El usuario edita su nombre, apellidos y contraseña.
El sistema valida los campos y actualiza el perfil del usuario.
El sistema muestra un mensaje de confirmación.
Flujos alternativos:

3a. El usuario intenta cambiar su email: el sistema valida que el email no esté registrado previamente.
5. Ver proyectos
Actores: Usuario registrado.

Precondiciones: El usuario ha iniciado sesión.

Flujo básico:

El usuario navega a la página de proyectos.
El sistema muestra una lista de proyectos publicados por desarrolladores.
El usuario puede hacer clic en un proyecto para ver más detalles.
El usuario puede mostrar/filtrar los proyectos a partir de un buscador
6. Publicar proyecto
Actores: Usuario registrado con perfil de desarrollador.

Precondiciones: El usuario ha iniciado sesión y su perfil es de desarrollador.

Flujo básico:

El usuario navega a la página de publicación de proyecto.
El usuario introduce el nombre, descripción, imagen representativa, enlaces de servidor y repositorio, estado y otra información relevante del proyecto.
El sistema valida los campos y crea un nuevo proyecto.
El sistema muestra un mensaje de confirmación y redirige al usuario a la página de proyectos.
Flujos alternativos:

2a. El desarrollador decide no publicar el proyecto y selecciona la opción de cancelar.
El sistema descarta la información ingresada en el formulario.
El sistema muestra un mensaje de confirmación al desarrollador.
7. Editar proyecto:
Actor principal: Desarrollador

Objetivo: Editar la información de un proyecto previamente creado.

Precondiciones: El usuario debe haber iniciado sesión como desarrollador y tener al menos un proyecto previamente creado.

Flujo principal:

El usuario selecciona la opción de "Editar proyecto".
El sistema muestra la lista de proyectos previamente creados por el usuario.
El usuario selecciona el proyecto que desea editar.
El sistema muestra el formulario de edición del proyecto con la información actual del mismo.
El usuario realiza los cambios necesarios en la información del proyecto y guarda los cambios.
El sistema valida la información ingresada por el usuario y actualiza la información del proyecto en la base de datos.
El sistema muestra una confirmación de que la información del proyecto ha sido actualizada correctamente.
8. Eliminar proyecto:
Actor principal: Desarrollador

Objetivo: Eliminar un proyecto previamente creado.

Precondiciones: El usuario debe haber iniciado sesión como desarrollador y tener al menos un proyecto previamente creado.

Flujo principal:

El usuario selecciona la opción de "Eliminar proyecto" del proyecto que desea eliminar.
El sistema muestra una confirmación de que el usuario está seguro de eliminar el proyecto seleccionado.
El usuario confirma que desea eliminar el proyecto.
El sistema elimina el proyecto de la base de datos y muestra una confirmación de que el proyecto ha sido eliminado correctamente.
El sistema actualiza la información de proyectos.
9. Ver/Editar usuario:
Actor principal: Usuario administrador

Objetivo: Editar la información de los usuarios registrados.

Precondiciones: El usuario debe haber iniciado sesión en la aplicación y tener rol administrador.

Flujo principal:

El usuario selecciona la opción de "Ver usuarios".
El sistema muestra una tabla con 'inputs' con los datos de los usuarios.
El administrador realiza los cambios necesarios en la información de los usuarios (incluido el rol y el estado) y guarda los cambios.
El sistema valida la información ingresada por el usuario y actualiza la información del usuario en la base de datos.
El sistema muestra una confirmación de que la información del perfil ha sido actualizada correctamente.
9. Eliminar usuario:
Actor principal: Usuario administrador

Objetivo: Eliminar usuario del sistema.

Precondiciones: El usuario debe haber iniciado sesión en la aplicación y debe tener rol administrador.

Flujo principal:

El usuario selecciona la opción de "Ver usuarios".
El sistema muestra una tabla con 'inputs' con los datos de los usuarios.
El administrador hace clic sobre el icono de eliminar usuario de la fila correspondiente.
El sistema informa de que se eliminarán todos sus registros.
El sistema muestra una confirmación de que la información de que el usuario ha sido borrado correctamente.
Errores
Vamos a repasar los diferentes casos de uso analizando el flujo principal y añadiendo los flujos alternativos para contemplar los posibles errores del sistema. Puedes considerar los siguientes mensajes:

Error de conexión: El servidor no puede establecer una conexión con la base de datos, lo que impide que se puedan realizar operaciones en la plataforma. El sistema debería mostrar un mensaje de error indicando que no se pudo conectar con la base de datos y ofrecer la posibilidad de volver a intentarlo o contactar con el soporte técnico.

Error de validación: Cuando el sistema recibe información del usuario, debe validarla para asegurarse de que cumple con los requisitos de formato y contenido necesarios. Si la información no es válida, el sistema debería mostrar un mensaje de error indicando el problema específico, como "El campo de correo electrónico debe ser una dirección de correo válida".

Error de autenticación: Si un usuario intenta acceder a una página o realizar una acción que requiere autenticación, pero no ha iniciado sesión o sus credenciales son incorrectas, el sistema debería mostrar un mensaje de error indicando que la acción no está autorizada y ofrecer la posibilidad de iniciar sesión o recuperar la contraseña.

Error de autorización: Si un usuario intenta realizar una acción que no está autorizada para realizar debido a su rol, el sistema debería mostrar un mensaje de error indicando que la acción no está autorizada y ofrecer la posibilidad de volver a la página anterior.

Error de servidor: En caso de que se produzca un error interno en el servidor, como una excepción no controlada, el sistema debería mostrar un mensaje de error genérico indicando que se produjo un error y ofrecer la posibilidad de volver a intentarlo o contactar con el soporte técnico.