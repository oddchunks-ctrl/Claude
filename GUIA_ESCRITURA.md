# Guía de escritura (mínimo de tokens, cero pérdida de información)

## 1. Principios
1. Cada dato en un solo sitio; en los demás, enlace (`PROYECTO.md §4`).
2. Estado, no narración. El "cómo se llegó" va en `HISTORIAL.md`, 1 línea.
3. Se sobrescribe lo que cambia y se borra lo obsoleto (queda en git).
4. Lo importante, primero. Sin relleno: ni saludos, ni introducciones, ni conclusiones que repiten.
5. Menos archivos que leer: lo que se lee siempre junto va en el mismo archivo.

## 2. Estilo
- Telegráfico: frases nominales o infinitivo. Ej.: "Revisar bonus de chunks".
- Tablas para ≥3 elementos con los mismos campos (≤5 columnas, sin columnas vacías). Listas antes que párrafos.
- `·` para enumerar en línea; `→` para flujos; `/` para alternativas o pares.
- Negrita solo para lo crítico. Sin emojis decorativos.
- Fechas ISO (`2026-11-24`), o `dd mmm` si el año es evidente. Números con unidad (`13,5 €/mes`).
- Términos fijos: la misma palabra para la misma cosa ("admisión", "fuga", "vídeo").
- Documentación en ES; textos públicos en EN, entre comillas.

## 3. Marcas
✅ aprobado/hecho · (no aprobada) · ⚠️ riesgo · `[ ]`/`[x]` tarea · (sin confirmar) dato deducido.

## 4. Abreviaturas (lista cerrada)
AB AmberBot · DC Discord · MC Minecraft · TT TikTok · YT YouTube · CTA llamada a la acción · CET hora de España · P2W pay-to-win · vis visualizaciones · seg seguidores.

## 5. Estructura de archivos
- Título de 1 línea, con la fecha de los datos si aplica. Secciones numeradas (`## 1.`) para citarlas como `§N`.
- Identificadores estables (`A1`, `D3`…); nunca se renumeran.
- Tamaños máximos y cómo dividir: `AMPLIACION.md §1 y §5`.
- README de cada rol: misión (1 línea) → índice → pendientes → ideas aparcadas.

## 6. Qué no guardar
- Imágenes: se resumen en texto. Solo se guardan como referencia en `referencias/` o `capturas/`, que no se leen por defecto.
- Material en bruto: en `referencias/`.
- Diálogos: solo el resultado (dato, decisión o tarea).
- Secretos, IPs, tokens y datos personales.

## 7. Comprobación al editar
¿Dato duplicado? → enlazar · ¿algo obsoleto? → borrar · ¿relleno o narración? → telegráfico · ¿decisión nueva? → `PROYECTO.md §0` · ¿hito? → `HISTORIAL.md` · ¿tamaño y marcas correctos?
