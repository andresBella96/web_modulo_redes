# 🌐 Todo sobre las redes · Web del módulo de Redes (25/26)

Repositorio de la página web estática utilizada como apoyo docente en el **módulo de Redes** del ciclo de FP.  
La web sirve como punto de referencia para el alumnado: explica conceptos básicos de redes de datos, muestra ejemplos guiados de prácticas y recoge material visual de las sesiones de clase.

Está pensada para ser:

- 📚 Didáctica y clara para estudiantes que empiezan desde cero.
- 💻 Técnicamente correcta y bien estructurada.
- 📱 Totalmente responsive, usable tanto en ordenador como en móvil.

---

## 🎯 Objetivos de la web

- Ofrecer una **introducción visual y sencilla** a conceptos fundamentales de redes:
  - Crimpado de cables de red.
  - Herramientas básicas de análisis y diagnóstico.
  - Concepto de subredes y organización de una red IP.
- Servir como **material de apoyo** antes de exámenes o prácticas.
- Funcionar como **ejemplo real de una web estática moderna** para el alumnado:
  - Estructura HTML5 semántica.
  - Uso de CSS puro para diseño, maquetación y componentes.
  - Menú responsive con hamburguesa sin JavaScript.

---

## 🧩 Contenido principal

La página está dividida en secciones accesibles desde el menú superior:

### 🏠 Inicio (`#inicio`)
- Presentación de la web como **sitio oficial del módulo de Redes**.
- Explicación general de qué se puede encontrar en la página.
- Pequeño resumen de los contenidos: crimpado, herramientas, subredes y galería.

### 🔧 Crimpar un cable de red (`#crimpar`)
- Explicación paso a paso de cómo crimpar un cable Ethernet siguiendo el estándar **T568B**.
- Descripción de:
  - Corte del cable.
  - Pelado de la funda.
  - Orden de colores.
  - Inserción en el conector RJ45.
  - Uso de crimpadora.
  - Comprobación con tester.
- Sección pensada para que el alumno pueda **repasar la práctica** de laboratorio.

### 🧪 Herramientas de análisis de redes (`#herramientas`)
- Descripción de algunas herramientas fundamentales:
  - `ping`
  - `ipconfig` / `ip addr`
  - Wireshark
  - `tracert` / `traceroute`
- Para cada herramienta se explica:
  - Para qué sirve.
  - Ejemplo de uso.
  - En qué situaciones se utiliza.

### 🧮 Subredes (`#tema-libre`)
- Introducción al concepto de **subred**:
  - Qué es una subred.
  - Relación entre red, hosts y máscara.
  - Ejemplo sencillo con una red `/24` dividida en dos subredes `/25`.
- Se explican las ideas clave:
  - Máscara de red.
  - Rangos de hosts.
  - Direcciones de red y broadcast.
- Sección pensada como **resumen teórico** complementario a los ejercicios de clase.

### 🖼️ Galería de fotos (`#galeria`)
- Galería responsive de imágenes relacionadas con el módulo:
  - Cables crimpados.
  - Racks y armarios de comunicaciones.
  - Herramientas de red.
  - Dispositivos como routers.
- La sección se puede ir actualizando con **fotos reales de prácticas**.

---

## 🛠️ Tecnologías y decisiones técnicas

Esta web está construida con:

- **HTML5**  
  - Estructura semántica (`<header>`, `<main>`, `<section>`, `<footer>`, `<nav>`, `<article>`, `<aside>`).
  - Navegación mediante anclas internas para moverse entre secciones.

- **CSS3 (sin frameworks)**  
  - **Flexbox** para la barra de navegación y disposición básica del header.
  - **CSS Grid** para:
    - Sección `hero` (portada con texto + tarjeta lateral).
    - Rejilla de herramientas.
    - Rejilla de subredes (sección "Subredes").
    - Galería de imágenes responsive.
  - **Diseño responsive** mediante media queries:
    - Reorganización de columnas a una sola columna en pantallas pequeñas.
    - Ajuste de la galería de 4 → 2 → 1 columna según ancho disponible.
  - **Menú hamburguesa con CSS puro**:
    - Uso de un `<input type="checkbox">` escondido como "interruptor".
    - Un `<label>` que actúa como icono hamburguesa.
    - Selectores como `:checked + label` y `:checked ~ .nav-links` para mostrar/ocultar el menú en móvil.
    - Animación de las tres líneas para formar una “X” al abrir el menú.
  - **Estética general**:
    - Fondo con **degradado** tipo “dashboard” oscuro.
    - Tarjetas con bordes redondeados, sombras suaves y transparencia.
    - Paleta basada en azules oscuros y acentos violetas.
    - Componentes tipo “pill” para etiquetas de temas y tags.

- **Favicon**
  - Integración de un icono PNG mediante:
    ```html
    <link rel="icon" type="image/png" href="favicon.png" />
    ```

- **Sin JavaScript**
  - Todo el comportamiento visual (incluyendo el menú responsive) se ha resuelto con HTML + CSS.
  - Adecuado como ejemplo de lo que se puede lograr con CSS puro.

---

## 📁 Estructura del proyecto

Estructura mínima del repositorio:

```bash
.
├── index.html        # Página principal de la web
├── favicon.png       # Icono de la pestaña del navegador
├── cabledered.jpg    # Imágenes usadas en la galería (ejemplo)
├── rack.jpg
├── crim.png
└── router.png
