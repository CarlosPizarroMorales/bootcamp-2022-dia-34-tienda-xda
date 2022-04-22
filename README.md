## Desafio "Tienda XDA"

|Bootcamp 2022 Modulo 3|Desarrollo de la interfaz de usuario Web|
|----|-----|
|**Unidad 4**|SVG, transitions & animations|
|**Día Bootcamp**|34|
|**Día Modulo**|12/15|

<hr>

Este desafío consiste en un frontend de un sitio web, no funcional (solo HTML y CSS). Entre los objetivos esperados se incluyen:
- Utilizar Sass y su patrón 7-1.
- Implementar una guía de estilos de forma modular. 
- Implementar las 3 mockups del proyecto.
- Utilizar y modificar al menos 1 elemento SVG.
- Agregar transiciones y animaciones en elementos a elección personal.

### NOTAS:

En un primer enfoque, consideraré realizarlo completamente con flex, distinguiendo 2 contenedores principales: 
  1. el contenedor del navbar que tendrá que tener otro contenedor flex para los ítems del menú que se mostrarán sobre el hero-banner en tamaños *mobile*, 
  2. y el contenedor del resto de la página que puede considerarse un `flex-column` con 3 elementos:
     1. hero-banner,
     2. contenido central,
     3. footer con suscribe invertido (`writing-mode: vertical-lr`) 
  3. Este `flex-column` solo cambia su espaciado en tamaño tablet pero en tamaño desktop debe presentarse como `flex-row-reverse`



<!--TODO Al definir layout final, afinar alineación vertical logo/toggle-button -->
<!--TODO Al definir layout final, afinar vh del hero-banner background -->
<!--TODO Al definir layout final, afinar margin-left de article / padding de suscribe -->
<!--TODO  #e3c7aa -->
<!--TODO  #ffe3be -->
<!--TODO  una animación entrete sería que el logo gire mientras crece hasta llegar a su posición y tamaño definido en el mockup -->
<!--TODO  se podría intentar una transición en el ul dropdown -->

<!--TODO  Mejorar botón con el svg de Bootstrap -->