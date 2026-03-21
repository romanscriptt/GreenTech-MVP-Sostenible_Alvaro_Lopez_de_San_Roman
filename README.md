# GreenTech MVP Sostenible
**Álvaro López de San Román — 1.º DAM**

---

## ¿Qué es este proyecto?

Una landing page refactorizada para la ONG GreenTech Solutions. El objetivo era limpiar un código lleno de librerías innecesarias y hacerlo más ligero, rápido y sostenible.

---

## ¿Qué se eliminó y por qué?

| Lo que había | Para qué se usaba realmente | Lo que lo reemplaza |
|---|---|---|
| Bootstrap CSS (~150 KB) | Solo para poner un botón verde | CSS nativo |
| Bootstrap JS (~16 KB) | Para nada | Eliminado |
| Font Awesome (~400 KB) | Un solo icono de hoja | Emoji 🌿 |
| jQuery (~87 KB) | Solo para añadir el footer | `document.getElementById()` |
| moment.js (~67 KB) | Solo para mostrar el año | `new Date().getFullYear()` |
| Google Fonts (5 variantes) | Solo se usaban 2 | Reducido a 2 variantes |

**Resultado: se pasó de ~780 KB a ~20 KB por visita. Un 97% menos.**

---

## ¿Por qué esto importa para el medio ambiente?

Cada vez que alguien carga una web, los servidores transfieren datos. Esa transferencia consume electricidad, y la electricidad genera CO₂.

Si una web pesa menos:
- Los servidores gastan menos energía → menos emisiones [1]
- El móvil trabaja menos → gasta menos batería
- Los móviles viejos no se quedan "lentos" por culpa del código → duran más → menos basura electrónica [2]

Según Verdecchia et al. [3], eliminar dependencias innecesarias es una de las prácticas más efectivas de Green Software Engineering.

---

## Técnicas aplicadas

- **CSS nativo** con variables `(:root)` en lugar de Bootstrap
- **Lazy loading** en imágenes: `loading="lazy"` — solo se descarga la imagen cuando el usuario la va a ver
- **JavaScript nativo** sin jQuery ni librerías externas
- **Fuentes optimizadas**: solo los pesos necesarios + `display=swap`

---

## Referencias (IEEE)

[1] W3C, "Web Sustainability Guidelines (WSG) 1.0," 2023. [Online]. Available: https://www.w3.org/TR/wsgl/

[2] Green Software Foundation, "Green Software Practitioner Course," 2024. [Online]. Available: https://learn.greensoftware.foundation/

[3] R. Verdecchia et al., "Green IT and Green Software Engineering: A Systematic Mapping Study," arXiv:2102.04945, 2021. [Online]. Available: https://arxiv.org/abs/2102.04945
