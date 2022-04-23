## Desafio "Tienda XDA"
![presentacion][0]

|Bootcamp 2022 Modulo 3|Desarrollo de la interfaz de usuario Web|
|----|-----|
|**Unidad 4**|SVG, transitions & animations|
|**Día Bootcamp**|34|
|**Día Modulo**|12/15|

<hr>

Este desafío consiste en un frontend de un sitio web, no funcional (solo HTML y CSS). Entre los objetivos esperados se incluyen:
- Utilizar Sass y su patrón 7-1. &#x2705;
- Implementar una guía de estilos de forma modular. &#x2705;
- Implementar las 3 mockups del proyecto. &#x2705;
- Utilizar y modificar al menos 1 elemento SVG. &#x2705;
- Agregar transiciones y animaciones en elementos a elección personal. &#x2705;

### IMPLEMENTACIóN

1. Como ejercicio, se ha implementado CSS Flex cuando fue necesario, prescindiendo de Bootstrap.
2. La estructura general es realmente simple: se consideran 3 grandes elementos: 
   1. El navbar, independiente en todo *breakpoint*,
   2. Un bloque `.main-banner` con la imagen principal, 
   3. Un bloque `.main-content` que tiene tanto el contenido de texto como la sección negra de suscribirse. 
3. Los dos últimos bloques se presentan según su *normal flow* hasta que se llega a la vista *desktop*, momento en que se los trata con `display: flex; flex-direction: row reverse` para lograr que la imagen quede detrás del contenido de texto. 
4. El elemento en vertical se ha tratado con `writing-mode: vertical-lr`
5. En el *approach* final, he tomado la sugerencia del profesor de hacerlo *responsive* pero se ha aplicado solo al breakpoint más grande. Esto porque en la práctica apuntar a un viewport de dispositivo móvil específico permite lograr una buena implementación de la idea del diseñador sin necesitar mayor flexibilidad, pero en viewports grandes, otorga cierta flexibilidad para mantener en lo posible la consistencia del diseño.
6. Se han utilizado dispositivos de Apple en el inspector de elementos como targets para trabajar en las distintas vistas porque ya en desafíos anteriores se han entregado solo dispositivos Apple como referencia y porque los viewports corresponden de forma exacta. Y debido a que hay alturas configuradas en `vh` el simular las mockups en *responsive* con largo continuo las romperá. 
   - iPhone 6/7/8 para vista *mobile* 375x667
   - ![screenshot1][1]
   - iPad para vista *tablet* 768x1024
   - ![screenshot2][2]
   - MacBook Pro/Air 13" para vista *desktop* 1280x800 (como custom device)
   - ![screenshot2][3]

7. En el último viewport, se ha establecido la condición `(min-width: 992px)` para el salto aunque el target es 1280x800. Esto para abarcar una cantidad mayor de dispositivos.
8. Se ha implementado una transición en los menús del dropdown de la vista mobile que responden al evento hover pero en el inspector deben ser clickeados para simular esta acción y poder observar la transición:
9. ![captura de proyecto][4]
10. Se ha implementado una animación descrita abajo en **NOTAS** que gira y hace crecer el logo hasta que llega a su posición y tamaño final.
11. ![captura de animación][5] 



### NOTAS:

- Si necesito aplicar dos transformaciones dentro de 1 mismo punto en un `@keyframe` no deben escribirse como reglas separadas, sino encadenadas: 

```css
/* ESTO NO FUNCA, SOLO EJECUTA EL ÚLTIMO */
@keyframes aparecer {
  0% {transform: scale(0); transform: rotate(0deg)};
  100% {transform: scale(1); transform: rotate(360deg)};
}

/* ESTO SI FUNCA */
@keyframes aparecer {
  0% {transform: scale(0) rotate(0deg)};
  100% {transform: scale(1) rotate(360deg)};
}
```

Una referencia en [Stackoverflow.][5]


[0]:./assets/img/presentacion.png
[1]:./assets/img/Screenshot2.png
[2]:./assets/img/Screenshot3.png
[3]:./assets/img/Screenshot4.png
[4]:./assets/img/Screenshot1.png
[5]:./assets/img/logo-animation.gif
[6]:https://stackoverflow.com/questions/14384494/multiple-css-keyframe-animations-using-transform-property-not-working



<!--TODO  Mejorar botón con el svg de Bootstrap -->
<!--TODO  Hacer un favicon?? -->
<!--TODO -LISTO- animación logo gire creciendo hasta asentarse -->
<!--TODO -LISTO- Eliminar esquema de color no utilizado -->
<!--TODO -LISTO- Dejar navbar fijo en 93px height a partir de 768px -->