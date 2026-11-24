# Cómo ampliar el repo sin perder la optimización
Se lee antes de **crear archivos, carpetas o roles**, o de integrar otro repo. La forma de escribir está en `GUIA_ESCRITURA.md`.

## 1. Presupuesto de lectura
| Qué | Límite |
|---|---|
| Lectura al empezar (`CLAUDE.md` + `PROYECTO.md`) | ≤ 10 KB |
| `CLAUDE.md` (se carga en cada sesión) | ≤ 1,5 KB; no crece al añadir roles |
| `PROYECTO.md` | ≤ 8 KB |
| `README.md` de un rol | ≤ 1,5 KB |
| Cualquier otro `.md` | ≤ 5 KB |

Comprobar los tamaños con `wc -c *.md */*.md`. Si se pasa uno, aplicar §5.

## 2. Estructura fija
```
raíz:    CLAUDE.md · PROYECTO.md · GUIA_ESCRITURA.md · AMPLIACION.md · HISTORIAL.md   (nada más)
<rol>/:  README.md · <tema>.md · referencias/ (material en bruto) · capturas/ (imágenes)
```
- Nombres en minúsculas, kebab-case y en español (`plan-contenido.md`).
- Nada de subcarpetas de temas dentro de un rol, salvo `referencias/` y `capturas/`.

## 3. Añadir un rol (solo si el usuario lo pide)
1. Crear `<rol>/README.md` con este orden: misión (1 línea) → §1 índice → §2 pendientes → §3 ideas aparcadas.
2. **Pasar** a ese rol las secciones de `PROYECTO.md` que le correspondan. En `PROYECTO.md` queda solo un resumen de 1–2 líneas y un enlace. Ej.: si se crea `comunidad/`, se lleva `PROYECTO.md §4` y §8.
3. Añadir el rol a la línea "Subroles" de `CLAUDE.md` (sin filas nuevas en la tabla).
4. Añadir 1 línea a `HISTORIAL.md`.

## 4. Añadir un documento
1. Comprobar antes si cabe en uno que ya existe. Si se va a leer siempre junto a otro, va en el mismo archivo.
2. Si es nuevo: una fila en el índice del README de su rol (nombre + qué contiene, en 1 línea).
3. El material en bruto (transcripciones, exportaciones, registros) va a `referencias/`, junto con un resumen en el documento de su tema.
4. Imágenes: solo como referencia, en `capturas/` o `referencias/`, y siempre resumidas en texto en el documento de su tema.

## 5. Cuando un archivo crece
- **Se divide por tema, no por fecha.** Ej.: `estadisticas-tiktok.md` → `estadisticas-tiktok.md` + `estadisticas-youtube.md`.
- **Los datos periódicos** (estadísticas, métricas) guardan solo la última toma completa más una tabla de evolución (1 fila por periodo). Las tomas antiguas se borran (quedan en git).
- **Lo terminado se borra:** vídeos publicados → 1 fila en la tabla de métricas; tareas `[x]` → fuera al cerrar la sesión.
- **`HISTORIAL.md` > 5 KB:** los meses anteriores se resumen en 1–3 líneas por mes.

## 6. Identificadores
- Cada ID es único en todo el repo y nunca se renumera ni se reutiliza.
- Marketing: ideas y vídeos `A1`–`J2`; nuevos pilares desde la `K`. Repeticiones de un formato: `H3 #2`.
- Rol nuevo: un prefijo de 3 letras + número (`COM-1`, `NEG-1`), anotado en su README.

## 7. Integrar el proyecto real (PC, Codex, AB)
1. Copiar estos archivos a la raíz del repo real. Si ya hay un `CLAUDE.md`, se fusionan respetando el límite de §1.
2. **Los documentos de código** (README de AB, etc.) se quedan donde están. Aquí solo se enlazan; no se copian.
3. **Los documentos del PC** (`ESTADO_PROYECTO.md`, `discord.md`, `HOSTING.md`, `REGLAS_SERVIDOR.md`):
   - Se extraen los hechos vigentes a `PROYECTO.md` o al rol que corresponda.
   - Los originales se marcan en `CLAUDE.md` como "no leer por defecto".
   - Nunca se copian secretos ni IPs.
4. Si hay datos contradictorios, manda el código o el documento más reciente. Avisar al usuario.

## 8. Al cerrar cada sesión
Estado actualizado · decisiones en `PROYECTO.md §0` · 1 línea en `HISTORIAL.md` · fuera lo obsoleto y las tareas `[x]` · tamaños dentro de §1 · índices al día · commit y push.
