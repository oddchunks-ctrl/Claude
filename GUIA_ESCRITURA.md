# Guía de escritura de la documentación
> Objetivo: que Claude lea los documentos con el **mínimo de tokens y sin perder información**. Obligatoria para cualquier archivo `.md` interno del repo.

## 1. Principios
1. **Cada dato en un solo sitio.** Si hace falta en otro archivo, se enlaza: `ver PROYECTO.md §4`. No se copia.
2. **Se describe el estado, no se narra.** Se escribe cómo están las cosas ahora, no cómo se llegó. El "cómo" va en `HISTORIAL.md`, en una línea.
3. **Se sobrescribe, no se acumula.** Cuando un dato cambia, se reemplaza. Lo obsoleto se borra (queda en git).
4. **Lo importante, primero:** dentro de cada archivo y de cada sección.
5. **Sin relleno.** Nada de saludos, introducciones, "como se ha comentado", "es importante destacar que" ni conclusiones que repiten.

## 2. Estilo
- **Telegráfico:** frases nominales y verbos en infinitivo. Ej.: "Revisar el bonus de chunks", no "Habría que revisar si el bonus…".
- **Listas y tablas antes que párrafos.** Una tabla cuando hay ≥3 elementos con los mismos campos. Máximo 5 columnas y sin columnas vacías.
- **Separadores en línea:** `·` para enumerar en una línea y `→` para secuencias o flujos.
- **Negrita** solo para lo crítico: como mucho 1–2 por bloque.
- **Números con su unidad y fechas ISO:** `13,5 €/mes`, `2026-11-24`.
- **Términos fijos:** usar siempre la misma palabra para la misma cosa (p. ej. "admisión", no "verificación", "alta" o "registro" según el día).
- **Idioma:** documentación interna en español; los textos de cara al público, en inglés y entre comillas.

## 3. Marcas de estado (vocabulario cerrado)
| Marca | Significado |
|---|---|
| ✅ | Aprobado o hecho |
| (no aprobada) | Idea o propuesta pendiente del usuario |
| ⚠️ | Riesgo o aviso |
| `[ ]` / `[x]` | Tarea pendiente / hecha |
| (sin confirmar) | Dato deducido, no verificado |

## 4. Abreviaturas permitidas (no inventar otras)
**AB** AmberBot · **DC** Discord · **MC** Minecraft · **TT** TikTok · **YT** YouTube · **CTA** llamada a la acción · **CET** hora peninsular española · **P2W** pay-to-win · **SQLite AB** base de datos de AmberBot.

## 5. Estructura de los archivos
- **Cabecera de una línea** (`>`) con el propósito y la fecha de los datos.
- **Encabezados cortos y numerados** (`## 1.`), para poder citar `§N`.
- **Identificadores estables** para lo que se cita (ideas `A1`…, vídeos `D3`…). Nunca se renumeran.
- **Tamaño máximo:** los archivos de estado, unos 10 KB; los demás, unos 5 KB. Si se superan, se dividen por tema y se añade la entrada en `CLAUDE.md` o en el README del rol.
- **README de cada rol:** misión (1 línea) → índice (tabla) → estado → pendientes → ideas aparcadas.

## 6. Qué no guardar en texto
- **Imágenes:** cuestan muchos tokens. Se resume en texto lo que contienen y la imagen se guarda solo si es material de referencia (`referencias/`, `capturas/`), que no se lee por defecto.
- **Material en bruto** (transcripciones, exportaciones, registros): en `referencias/`, marcado en `CLAUDE.md` como "solo si hace falta".
- **Secretos, IPs, tokens y datos personales de miembros:** nunca.
- **Conversaciones:** solo se guarda el resultado (dato, decisión o tarea), no el diálogo.

## 7. Comprobación al editar
- [ ] ¿El dato ya existía en otro archivo? → Se enlaza, no se duplica.
- [ ] ¿Ha quedado algo obsoleto? → Se borra.
- [ ] ¿Hay frases de relleno o narrativas? → Se pasan a estilo telegráfico.
- [ ] ¿Hay decisión nueva? → Va a `DECISIONES.md`. ¿Hito? → Una línea en `HISTORIAL.md`.
- [ ] ¿Se respetan el tamaño máximo y las marcas de estado?
