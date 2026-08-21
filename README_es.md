# 🐾 わんこノート (Wanko Note)

Es una app web sencilla para registrar la salud y el cuidado diario de un perro. Permite anotar en el momento comida, paseo, popó, medicina y cualquier cosa que llame la atención. Está pensada especialmente para poder consultar después "qué pasó ese día", sobre todo con perros mayores o con alguna condición médica.

La app funciona solo en el navegador. Los registros de `demo.html` se guardan solo en ese mismo dispositivo (localStorage). (`index.html` es la versión con sincronización en la nube, la excepción explicada más abajo).

---

## Archivos

| Archivo | Uso | URL |
|---|---|---|
| `demo.html` | **La versión principal, la que usa todo el mundo.** Guarda los registros de tu propio perro en tu propio dispositivo | https://ogurayu-coder.github.io/Toriaezu/demo.html |
| `index.html` | Versión de sincronización en la nube de Mo. Se usa solo cuando Mo y el veterinario necesitan compartir los registros durante un viaje | https://ogurayu-coder.github.io/Toriaezu |

`index.html` y `demo.html` guardan los datos con claves distintas, así que aunque se abran ambos en el mismo dispositivo, los datos no se mezclan.

### ⚠️ Sobre `index.html` (importante)

`index.html` es la versión que sincroniza con la nube (Firebase), y **se usa solo durante los viajes, cuando Mo y el veterinario necesitan compartir los mismos registros. Para tus propios registros, siempre usa `demo.html`.** Escribir en `index.html` afecta directamente los datos reales de Mo en la nube, así que no escribas ahí, salvo que seas el veterinario de Mo registrando algo durante su viaje (verla está bien, no hay problema).

---

## Sobre cómo se guardan los datos (importante)

**Lo que sigue es sobre `demo.html` (la versión principal). `index.html` sincroniza con la nube, así que no aplica (ver arriba).**

- Los registros se guardan **solo en ese navegador, en ese dispositivo (localStorage)**. No se comparten automáticamente con otros dispositivos ni con la nube.
- Aunque sea el mismo enlace, si el dispositivo es distinto (por ejemplo un iPhone y un iPad), los datos se guardan por separado.
- **Si se abre en modo privado (incógnito), los datos desaparecen en cuanto se cierra la pestaña.** Para el uso normal, abrir siempre en modo normal de Safari.
- **Si en Safari se usa "Borrar historial y datos de sitios web", los registros guardados en ese dispositivo se pierden por completo.** No hay forma de recuperarlos después, así que antes de hacer limpieza de almacenamiento o solucionar algún problema en el iPhone, siempre conviene sacar un respaldo primero.
- Agregar el ícono a la pantalla de inicio ayuda a abrir siempre desde el mismo lugar (botón Compartir en Safari → "Agregar a pantalla de inicio").

---

## Cuando Mo viaja

Durante el viaje de Mo se usa `index.html` (la versión con sincronización en la nube). Cuando Mo y su veterinario abren el mismo enlace de `index.html`, los registros se sincronizan automáticamente a través de Firebase, así que no hace falta copiar y pegar el respaldo cada vez. Al terminar el viaje, se vuelve a usar `demo.html` para el uso diario normal.

**Este método es exclusivo de Mo.**

---

## Respaldo

Desde "Ver respaldo" dentro de la app se puede exportar todo (registros + lista de perritos) como texto. Con solo presionar el botón "Copiar" se copia automáticamente; conviene guardarlo en una app de notas. Para restaurarlo, se pega ese mismo texto en "Restaurar respaldo".

**Antes de agregar o borrar un perrito, o antes de usar "Borrar datos de sitios web" en el iPhone, siempre hay que sacar un respaldo primero.**

### Al cambiar de dispositivo

Como localStorage guarda los datos por dispositivo, **no se transfieren automáticamente a uno nuevo.** Antes de cambiar de dispositivo, hay que mover el respaldo con estos pasos:

1. En el dispositivo anterior, abrir la app → "Ver respaldo" → presionar "Copiar"
2. Abrir un **correo dirigido a uno mismo**, pegar el texto tal cual en el cuerpo y enviarlo (no hace falta adjuntarlo como archivo; pegarlo en el cuerpo del correo es lo más seguro)
3. En el dispositivo nuevo, abrir ese mismo correo y copiar el texto pegado
4. En el dispositivo nuevo, abrir la app → "Restaurar respaldo" → pegar el texto

Si se salta este paso, el dispositivo nuevo empezará completamente vacío, sin ningún registro anterior.

---

## Comentarios y sugerencias

Si encuentras algún error o tienes alguna idea de función nueva, puedes escribirla con confianza en este [formulario de Google](https://forms.gle/s97kzuBfatnangPs5). También son bienvenidos los [Issues](../../issues).

---

## Funciones principales

- Registro de comida, paseo, popó, medicina y notas (con hora y comentario)
- Registro de vacunas y desparasitación, con seguimiento del último registro y la próxima fecha (avisa con colores cuando se acerca el vencimiento)
- Vista de calendario (para ver de un vistazo los días con alguna nota)
- Búsqueda por palabra libre (ej: vómito, convulsión), busca dentro del texto de las notas
- Agregar registros de días pasados (tocando la fecha en el calendario)
- Exportar y restaurar respaldos
- Agregar, editar o borrar perritos desde "🐾 Administrar perritos"

---

## Historial de cambios (notas breves)

- Corregido un desfase de zona horaria (los registros nocturnos aparecían en el día siguiente)
- Corregido un error por el que los registros borrados volvían a aparecer
- Ahora se puede elegir la cantidad de perritos y su apariencia (forma de orejas, patrón, color)
- Función para agregar, editar y borrar cada perrito, e inclusión de la lista de perritos en el respaldo
- `index.html` quedó como la versión de sincronización que Mo y el veterinario usan durante los viajes; `demo.html` sigue siendo la versión principal para el uso diario de todos

---

*Para dudas técnicas sobre el desarrollo de la app, ver README.md (en japonés).*
