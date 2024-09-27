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