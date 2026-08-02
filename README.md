#  [Nombre de tu Proyecto / Motor] — v1.3

> Un motor/juego retro en Java inspirado en las mecánicas y estética clásica de Minecraft.

![Version](https://img.shields.io/badge/version-1.3-brightgreen.svg)
![Language](https://img.shields.io/badge/language-Java-orange.svg)
![Build](https://img.shields.io/badge/build-passing-success.svg)

---

##  Sobre el Proyecto

Este proyecto es un motor de juego en 3D desarrollado en **Java**, diseñado para aprender y asi logrando: renderizar bloques, entidades y mapas usando texturas en formato atlas y modelos personalizados.

En esta **versión 1.3**, se han integrado avances clave en el renderizado de mapas de textura (`terrain.png`), la fragmentación de sprites individuales y la implementación de entidades 3D personalizadas (como modelos de cerdos y bloques funcionales, asi como el Multiplayer en fase temprana).

---

##  Novedades en la Versión 1.3

*  **Modelado de Entidades:** Integración de la clase `CustomModel` para renderizar entidades dinámicas (ej. Cerdo con texturas oficiales 64x64).
*  **Mapeo de Atlas UV:** Soporte mejorado para coordenadas de atlas de texturas históricas (`terrain.png` de Minecraft 1.0.0 a 1.4.7).
*  **Carga Individual de Sprites:** Compatibilidad con texturas $16 \times 16$ desglosadas por casillas/tiles.
*  **Optimización de Renderizado:** Ajustes en los puntos de pivote para animaciones de extremidades y rotaciones.

---

##  Tecnologías Utilizadas

* **Lenguaje:** Java (JDK 8+)
* **Gráficos / Render:** LWJGL / OpenGL *(Ajusta si usas otra librería)*
* **Modelado 3D:** Blockbench
* **Formato de Archivos:** `.java` (Custom Models) / `.png` (Atlas $256 \times 256$ y $64 \times 64$)

---

##  Estructura del Proyecto

```text
src/
├── assets/
│   └── textures/
│       ├── blocks/       # Sprites individuales (tile000.png, etc.)
│       ├── entity/       # Textura del cerdo y otras entidades (64x64)
│       └── terrain.png   # Atlas completo histórico 256x256
├── models/
│   └── CustomModel.java  # Renderizador de entidades exportado desde Blockbench
└── engine/
    └── Main.java         # Bucle principal del juego
