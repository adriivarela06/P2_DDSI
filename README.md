# DocuGest · Análisis funcional del sistema

Este repositorio recoge el modelado funcional y el análisis de flujo de datos de DocuGest, un sistema de gestión documental diseñado para centralizar archivos corporativos, controlar versiones y auditar consultas.

## Contenido del repositorio

El proyecto agrupa tanto los ficheros fuente editables de los diagramas como la documentación y las herramientas de visualización:

* **Diagramas de flujo de datos (DFD):** Modelado jerárquico del sistema en formato `.drawio` / `.xml`, estructurado desde el diagrama de contexto hasta la descomposición por procesos.
* **Diagrama de caja negra:** Representación de alto nivel con las entradas y salidas globales del sistema.
* **Esquemas externos:** Vistas parciales de entidades y relaciones asociadas a cada subsistema y almacén de datos.
* **Visor interactivo:** Aplicación web autocontenida en HTML (`dfd_zoom_interactivo.html`) que permite navegar entre los niveles de detalle de los diagramas mediante zoom.
* **Memoria de la práctica:** Documento técnico (`Practica2_DDSI.docx`) con la especificación de flujos, almacenes y seguimiento del trabajo.

## Arquitectura general del modelo

El análisis se organiza de forma descendente en tres niveles de abstracción:

1. **Nivel 0 (Diagrama de contexto):** Muestra la interacción entre el sistema como unidad central y los tres agentes externos principales (Administración, Sistema de Personal y Usuario).
2. **Nivel 1 (Subsistemas):** Descompone la funcionalidad en cinco procesos principales conectados a través de cinco almacenes de datos compartidos:
   * Gestión de identidad y accesos
   * Repositorio y control de versiones
   * Revisión y aprobación
   * Organización, categorías y búsqueda
   * Auditoría y estadísticas
3. **Nivel 2 (Subprocesos):** Detalla las operaciones internas de cada módulo a partir de los requisitos funcionales definidos.

## Cómo visualizar y editar los archivos

* **Visor web:** Abre el archivo `dfd_zoom_interactivo.html` directamente en cualquier navegador moderno. Puedes hacer clic sobre cada proceso para descender de nivel y utilizar la tecla `Esc` o el botón superior para retroceder.
* **Edición de diagramas:** Los ficheros `.xml` y `.drawio` pueden abrirse y modificarse directamente desde la aplicación de escritorio o la versión web de [diagrams.net](https://app.diagrams.net/).
