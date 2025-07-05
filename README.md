# Proyecto Web UNISANGIL

Este es un proyecto de sitio web estático para UNISANGIL. Incluye una página de inicio y una página dedicada al Consultorio Tecnológico, ambas diseñadas para ser modernas y responsivas utilizando el framework Bootstrap y otras librerías de animación y diseño.

## Estructura de Archivos

El proyecto se compone de los siguientes archivos principales:

- **`index.html`**: Es la página de inicio del sitio. Contiene un carrusel de imágenes, accesos directos a servicios, tarjetas informativas sobre los programas académicos y una sección que destaca la experiencia de la universidad.
- **`consultorioTecnologico.html`**: Una página específica que detalla la información del Consultorio Tecnológico. Incluye secciones para la Misión y Visión, y un completo catálogo de tecnologías y portafolio de servicios presentados en formato de acordeón.
- **`styless.css`**: La hoja de estilos personalizada que aplica a ambos archivos HTML. Define la paleta de colores, tipografías, y estilos para componentes personalizados, asegurando una apariencia coherente en todo el sitio.
- **`README.md`**: Este archivo de documentación.

## Cómo Visualizar el Proyecto

Para ver el sitio web, simplemente abre los archivos `index.html` o `consultorioTecnologico.html` en cualquier navegador web moderno (como Google Chrome, Firefox, o Microsoft Edge).

```bash
# Ejemplo en un entorno de línea de comandos (opcional)
start index.html
```

## Tecnologías Utilizadas

- **HTML5**: Para la estructura y el contenido de las páginas.
- **CSS3**: Para los estilos personalizados y el diseño visual.
- **Bootstrap 5.3.3**: Framework principal para el diseño responsivo, la rejilla (grid system) y los componentes de interfaz de usuario.
- **Font Awesome 6.5.2**: Para la iconografía utilizada en todo el sitio.
- **Google Fonts**: Se utilizan las fuentes `Montserrat` y `Open Sans` para la tipografía.
- **Animate.css**: Para añadir animaciones a elementos específicos.
- **AOS (Animate On Scroll)**: Para animar elementos a medida que el usuario se desplaza por la página.

---

## Descripción de Secciones Visuales y Estilos CSS

A continuación, se describen las secciones visuales más importantes y las clases CSS que les dan estilo.

### 1. Encabezado y Navegación
- **Propósito**: El encabezado sirve como la identidad visual principal del sitio y el punto de acceso a la navegación global. Su diseño fijo (`sticky-top`) asegura que el logo y los enlaces de navegación estén siempre visibles, facilitando la exploración del usuario.
- **Estructura**: Se compone de dos partes principales:
    - **Barra Superior de Enlaces de Acceso Rápido**: Un `div` (`.bg-white .text-end .py-2 .px-5 .small .border-bottom .d-none .d-lg-block .fw-semibold`) que contiene enlaces a secciones clave como 'Aspirante', 'Estudiante', 'Graduados' y 'Empleados'. Está diseñada para ser visible solo en pantallas grandes (`.d-lg-block`).
    - **Barra de Navegación Principal**: Una etiqueta `<nav>` (`.navbar .navbar-expand-lg .bg-light .shadow-sm`) que alberga el logo de la universidad (`<a class="navbar-brand">` con una imagen `<img>`) y un menú de navegación colapsable (`<div class="collapse navbar-collapse">`). Este menú incluye elementos de lista (`<ul>` con `<li>`) para las secciones principales y un menú desplegable (`.nav-item .dropdown`) para 'Formación' y 'Nosotros', que a su vez contienen sub-enlaces organizados en columnas (`.row` con `.col-md-3`).
- **Archivos**: `index.html`, `consultorioTecnologico.html`
- **Clases CSS Clave**:
    - `.sticky-top`: Mantiene el encabezado visible en la parte superior de la pantalla.
    - `.navbar`, `.navbar-expand-lg`: Clases de Bootstrap para la barra de navegación, que la hacen responsiva y expandible en pantallas grandes.
    - `.dropdown-menu`, `.dropdown-item`: Estilizan los menús desplegables y sus elementos, con personalizaciones en `styless.css` para cambiar colores y efectos al pasar el ratón (`:hover`).
    - `.nav-item`: Aplica estilos a los elementos individuales de la navegación, incluyendo transiciones para efectos visuales suaves.

### 2. Carrusel de Imágenes (Página de Inicio)
- **Propósito**: El carrusel es el componente visual principal en la página de inicio, diseñado para captar la atención del usuario con imágenes dinámicas y mensajes promocionales clave. Su función es destacar programas académicos o eventos importantes de la universidad.
- **Estructura**: Se implementa utilizando un `div` principal (`<div id="mainCarousel" class="carousel slide">`) que contiene múltiples diapositivas (`.carousel-item`). Cada diapositiva es un `div` con una imagen de fondo (`background-image`) y contenido textual superpuesto (título, subtítulo y un badge). Los controles de navegación (flechas) permiten al usuario moverse entre las diapositivas.
- **Archivo**: `index.html`
- **Clases CSS Clave**:
    - `.carousel-slide`: Define la altura y el fondo de cada diapositiva del carrusel, incluyendo un degradado oscuro para mejorar la legibilidad del texto.
    - `.carousel-item`: Contenedor para cada diapositiva, gestionado por la funcionalidad de carrusel de Bootstrap.
    - `.text-warning`: Utilizada para resaltar texto clave dentro del carrusel, como el nombre de los programas o estados de inscripción.

### 3. Tarjetas de Programas (Página de Inicio)
- **Propósito**: Esta sección tiene como objetivo presentar de manera visual y organizada los diferentes niveles de formación académica que ofrece la universidad (Técnico, Pregrado, Posgrado, Educación Continua). Cada tarjeta actúa como un punto de entrada a información más detallada sobre el programa correspondiente.
- **Estructura**: Se compone de una cuadrícula responsiva de cuatro tarjetas (`<div class="card h-100 shadow-sm">`), cada una con una imagen representativa (`<img>`), un título (`<h5>`) y un botón de "Ver más" (`<a>`). Las tarjetas están diseñadas para tener una altura uniforme (`h-100`) y un efecto de sombra (`shadow-sm`) para destacarse. Al pasar el ratón sobre el botón, este cambia de estilo para indicar interactividad.
- **Archivo**: `index.html`
- **Clases CSS Clave**:
    - `.card`: Estilo base de la tarjeta con bordes redondeados (`border-radius: 16px`) y transiciones suaves para efectos de interacción.
    - `.card-img-top`: Ajusta la imagen en la parte superior de la tarjeta, asegurando que cubra el área designada (`object-fit: cover`).
    - `.card-title`: Define el estilo del título de la tarjeta, utilizando el color primario de la marca para coherencia visual.
    - `.btn-outline-warning`: Botón con un borde de color, que cambia a un fondo sólido y aumenta ligeramente de tamaño al pasar el ratón (`:hover`), proporcionando retroalimentación visual al usuario.
    - `.bg-split`: Crea un fondo dividido (mitad blanco, mitad azul) para la sección que contiene las tarjetas, añadiendo un toque de diseño distintivo.

### 4. Catálogo y Portafolio (Página Consultorio)
- **Propósito**: Esta sección tiene como objetivo presentar de forma organizada y accesible el catálogo de tecnologías y el portafolio de servicios ofrecidos por el Consultorio Tecnológico. Utiliza acordeones anidados para permitir al usuario explorar la información de manera interactiva y detallada sin sobrecargar la interfaz.
- **Estructura**: Se divide en dos columnas principales, cada una con una tarjeta (`.card`) que contiene un acordeón (`<div class="accordion">`). El acordeón principal (`#catalogoAccordion` o `#portafolioAccordion`) agrupa categorías generales, y dentro de cada categoría, se pueden encontrar sub-acordeones (`#equiposSubAccordion`, `#softwareSubAccordion`, etc.) para desglosar la información en niveles más específicos. Cada elemento del acordeón (`.accordion-item`) tiene un encabezado (`.accordion-header`) con un botón (`.accordion-button`) para expandir/contraer su cuerpo (`.accordion-body`).
- **Archivo**: `consultorioTecnologico.html`
- **Clases CSS Clave**:
    - `.accordion`, `.accordion-item`: Clases de Bootstrap para la estructura y funcionalidad del acordeón.
    - `.accordion-button`: Estiliza el botón que expande y contrae el contenido, personalizando su color y fuente para alinearse con la marca.
    - `.accordion-body`: Contenedor del contenido del acordeón, con un color de fondo suave para mejorar la legibilidad.
    - `.card-header`: Encabezado de las tarjetas que contienen los acordeones, utilizando el color de fondo `.bg-warning` para una distinción visual clara.

### 5. Modales de Misión y Visión (Página Consultorio)
- **Propósito**: Los modales (`modal`) se utilizan para mostrar información detallada sobre la misión y visión del Consultorio Tecnológico en ventanas emergentes. Esto permite presentar contenido extenso sin navegar a una nueva página, manteniendo al usuario en el contexto actual y mejorando la experiencia de usuario.
- **Estructura**: Cada modal es un `div` (`<div class="modal fade" id="modalVision" ...>`) que se activa mediante un botón o tarjeta (`.card-modal`) con atributos `data-bs-toggle="modal"` y `data-bs-target="#modalId"`. Contienen un encabezado (`.modal-header`) con un título y un botón de cierre, un cuerpo (`.modal-body`) para el contenido principal (párrafos de texto), y un pie de página (`.modal-footer`) con botones de acción. La clase `.fade` proporciona una transición suave al abrir y cerrar el modal.
- **Archivo**: `consultorioTecnologico.html`
- **Clases CSS Clave**:
    - `.modal`, `.modal-dialog`, `.modal-content`: Clases de Bootstrap que controlan el comportamiento, tamaño y estilo del modal.
    - `.modal-header`: Encabezado del modal, estilizado con un fondo degradado (`.bg-gradient-primary`) para un diseño moderno.
    - `.card-modal`: Clase personalizada para las tarjetas que activan los modales, añadiendo una animación de escala (`transform: scale(1.1)`) y sombra al pasar el ratón, lo que indica que son elementos interactivos.

### 6. Pie de Página
- **Propósito**: El pie de página proporciona información esencial de contacto, enlaces rápidos a secciones importantes del sitio y acceso a las redes sociales de la universidad. Su consistencia en ambas páginas asegura que el usuario siempre pueda encontrar esta información vital, mejorando la usabilidad y la accesibilidad.
- **Estructura**: Se implementa con una etiqueta `<footer>` (`<footer class="footer ...">`) que contiene un contenedor (`.container`) con tres columnas (`.row` con `.col-md-4`). Cada columna organiza la información de manera lógica: contactos (direcciones y teléfonos), enlaces rápidos (listas no ordenadas `<ul>` de enlaces `<a>`), y redes sociales (iconos de Font Awesome `<i>` dentro de enlaces `<a>`). Una línea horizontal (`<hr>`) separa la información principal de la sección de derechos de autor.
- **Archivos**: `index.html`, `consultorioTecnologico.html`
- **Clases CSS Clave**:
    - `.footer`: Clase principal que define el color de fondo oscuro (`#003366`) y el padding general del pie de página.
    - `footer .text-warning`: Personaliza el color de los títulos dentro del pie de página para que coincida con la paleta de la marca, asegurando coherencia visual.
    - `footer a:hover`: Añade un efecto de subrayado al pasar el ratón sobre los enlaces, indicando interactividad.

### 7. Funcionalidad del Robot Interactivo
- **Propósito**: Este componente añade un elemento interactivo y visualmente atractivo al sitio web. El robot actúa como un punto de interés que puede ser utilizado para futuras funcionalidades (e.g., un chatbot, un asistente virtual). Su animación de entrada lo hace notorio, y la animación de salida al hacer clic proporciona una experiencia de usuario fluida y controlada.
- **Estructura**: Se implementa como un `div` (`<div id="robotOverlay" class="robot-overlay animate__animated">`) que contiene la imagen del robot (`<img src="robot.png" alt="Robot">`). Este `div` se posiciona de forma fija en la esquina inferior derecha de la pantalla. La interactividad y las animaciones se controlan mediante JavaScript y clases CSS.
- **Archivos**: `index.html`, `consultorioTecnologico.html`, `styless.css`
- **JavaScript Clave**:
    - `document.addEventListener('DOMContentLoaded', function() { ... });`: Asegura que el script se ejecuta solo después de que todo el DOM ha sido cargado, evitando errores de elementos no encontrados.
    - `const robot = document.getElementById('robotOverlay');`: Obtiene una referencia al elemento del robot por su ID.
    - `robot.classList.add('animate__fadeInUp');`: Aplica la clase de `Animate.css` para la animación de entrada (`fadeInUp`) una vez que el DOM está listo.
    - `robot.addEventListener('click', function() { ... });`: Añade un "escuchador" de eventos para detectar clics en el robot.
    - `robot.classList.remove('animate__fadeInUp');`: Elimina la clase de animación de entrada para permitir que la animación de salida se reproduzca correctamente.
    - `robot.classList.add('animate__fadeOutDown');`: Aplica la clase de `Animate.css` para la animación de salida (`fadeOutDown`).
    - `robot.addEventListener('animationend', () => { robot.classList.add('hidden'); }, { once: true });`: Escucha el evento `animationend` para saber cuándo ha terminado la animación de salida. Una vez finalizada, añade la clase `hidden` para ocultar completamente el elemento. El `{ once: true }` asegura que este "escuchador" se elimine automáticamente después de ejecutarse una vez, optimizando el rendimiento.
- **Clases CSS Clave**:
    - `.robot-overlay`: Define la posición fija (inferior derecha), un `z-index` alto (`9999`) para asegurar que esté por encima de otros elementos, y el tamaño general del contenedor del robot.
    - `.robot-overlay img`: Ajusta el tamaño de la imagen del robot dentro de su contenedor.
    - `.hidden`: Una clase simple (`display: none;`) que se añade al elemento después de la animación de salida para ocultarlo completamente del flujo del documento.
    - `animate__animated`, `animate__fadeInUp`, `animate__fadeOutDown`: Clases proporcionadas por la librería `Animate.css` que definen las animaciones de entrada y salida, respectivamente.

### 8. Integración del Chatbot
- **Propósito**: La integración del chatbot tiene como objetivo proporcionar asistencia instantánea a los usuarios, responder preguntas frecuentes y mejorar la interacción general con el sitio web. Utiliza la plataforma Botpress para gestionar las conversaciones y la lógica del chatbot.
- **Tecnología**: Botpress es una plataforma de código abierto para construir, implementar y gestionar chatbots impulsados por IA. Permite crear flujos de conversación complejos, integrar servicios externos y personalizar la experiencia del usuario.
- **Estructura de la Integración**: La integración se realiza a través de la inclusión de scripts JavaScript proporcionados por Botpress directamente en los archivos HTML (`index.html` y `consultorioTecnologico.html`). Estos scripts son responsables de cargar el widget del chatbot en la página y establecer la conexión con el servidor de Botpress.
- **Archivos JavaScript Clave**:
    - `connection.js`: Este archivo probablemente contiene la configuración inicial para la conexión con la instancia de Botpress, como la URL del servidor de Botpress y el ID del bot. Es crucial para establecer la comunicación entre el frontend del sitio web y el backend del chatbot.
    - `chatbot.js`: Este archivo es el script principal del widget del chatbot. Contiene el código necesario para renderizar la interfaz del chatbot en la página, manejar las interacciones del usuario, enviar mensajes a Botpress y mostrar las respuestas del bot. Es el componente visible y funcional del chatbot en el sitio.

---

## Estilos CSS (`styless.css`)

El archivo `styless.css` contiene todos los estilos personalizados que complementan y sobrescriben las reglas de Bootstrap para adaptar el diseño a la identidad visual de UNISANGIL. Está organizado por secciones lógicas para facilitar su mantenimiento y comprensión.

- **Organización**: Los estilos están agrupados por componentes o secciones del sitio (e.g., `FUENTE PRINCIPAL`, `CARRUSEL`, `MENÚ DE NAVEGACIÓN`, `BOTONES DE ACCESO RÁPIDO`, `TARJETAS`, `BOTONES DE ADVERTENCIA`, `SECCIÓN EXPERIENCIA`, `PIE DE PÁGINA`, `CLASES DE UTILIDAD`, `CAJA DE INFORMACIÓN`, `TÍTULO DE SECCIÓN`, `TARJETA MODAL`, `MODAL`, `ACORDEÓN`, `ESTILOS DE ACORDEÓN ANIDADO`, `ESTILOS PARA EL ASISTENTE DE CHATBOT`, `MEDIA QUERIES`, `ANIMACIONES`, `Estilos para la imagen del robot superpuesta`, `Clase para ocultar elementos`).
- **Personalización**: Se ajustan propiedades como `font-family`, `background-color`, `color`, `padding`, `margin`, `border-radius`, `box-shadow`, y `transition` para crear una experiencia visual única.
- **Responsividad**: Incluye `@media queries` para adaptar el diseño a diferentes tamaños de pantalla, asegurando que el sitio sea completamente responsivo.
- **Transiciones y Efectos**: Se utilizan propiedades `transition` para suavizar los cambios de estado (e.g., `:hover`) y se integran librerías como `Animate.css` y `AOS` para efectos visuales dinámicos.
