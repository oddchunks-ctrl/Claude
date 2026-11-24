# Contexto del proyecto — registro de sesión provisional

> Este documento recoge todo lo hablado y hecho en una sesión provisional de Claude Code en la nube,
> mientras el repositorio real del proyecto está en el PC local (fuera de Claude).
> **Propósito:** adjuntarlo en el futuro proyecto (con el repositorio completo) para que el asistente
> tenga todo el contexto acumulado desde el principio.

---

## 1. Situación de partida

- **Fecha de inicio:** 2026-11-24
- El proyecto real vive en el PC del usuario, en un repositorio local (proyecto de Codex).
- El usuario no está en casa y no puede adjuntar el proyecto desde el dispositivo actual.
- Esta sesión en la nube se usa como **espacio provisional** para ir dando contexto.
- Repositorio provisional usado aquí: `oddchunks-ctrl/claude`, rama `claude/project-context-documentation-q9yr6t` (estaba vacío al empezar).

## 2. Descripción del proyecto

### AMBERGATES SMP

- **Qué es:** servidor de Minecraft SMP Vanilla.
- **Objetivo:** comunidad técnica y de construcción, de ambiente casual, con proyectos comunitarios (granjas, etc.).
- **Base técnica (resumen):**
  - Fabric + Lithium en el servidor, pero se puede entrar con el cliente Vanilla sin instalar nada.
  - Varios mods programados a medida para la gestión.
  - Algunos datapacks que no alteran la experiencia Vanilla.
  - Hosting: PebbleHost, 8 GB de RAM.
  - Conectado con Discord mediante RCON.
- **Discord:**
  - Unos 30 miembros. El servidor de Discord todavía está "verde" (poco desarrollado).
  - Bot propio: **AmberBot**, alojado en Railway. Tiene su propio repositorio en GitHub (el usuario lo compartirá cuando esté en su PC).
- **Estado actual:** servidor ya lanzado.

> Nota: en esta sesión provisional **no** se tratan los detalles técnicos del servidor de Minecraft.
> El foco aquí es el proyecto en conjunto: **marca, redes sociales y plan de negocio a futuro**.

## 3. Decisiones tomadas

| Fecha | Decisión | Motivo |
|-------|----------|--------|
| 2026-11-24 | Llevar un registro en `CONTEXTO_PROYECTO.md` con todo lo hablado | Poder pasarlo al proyecto definitivo cuando haya acceso al repositorio |
| 2026-11-24 | En esta sesión no se tocan temas técnicos del servidor; solo marca, redes y negocio | Preferencia del usuario |
| 2026-11-24 | **Objetivo del proyecto: hobby que se pague solo y deje algo de beneficio extra** | Definido por el usuario. No se busca escalar a red de servidores ni vivir de ello |

### Implicaciones del objetivo (hobby autofinanciado + algo de beneficio)
- Prioridad 1: cubrir los costes fijos (PebbleHost + Railway) con ingresos recurrentes.
- Prioridad 2: un pequeño excedente para mejoras, eventos, premios o beneficio personal.
- Mantener una carga de trabajo baja: nada de monetización que exija mucho tiempo de gestión.
- No sacrificar la esencia Vanilla ni la comunidad por ingresos (va contra la EULA y además espantaría al público técnico).
### Costes actuales (aprox.)
| Concepto | Coste mensual | Notas |
|----------|---------------|-------|
| PebbleHost (8 GB) | ~9 € | Servidor de Minecraft |
| Railway (AmberBot) | 5 USD (~4,5 €) | Saldo mensual; lo que no se gasta se acumula al mes siguiente |
| **Total** | **~13,5 €/mes (~160 €/año)** | |

### Objetivos de ingresos propuestos
- **Nivel 1 – Cubierto:** ~15 €/mes (costes más el margen que se llevan las plataformas de pago).
- **Nivel 2 – Con margen:** ~25 €/mes (costes más ~10 € para eventos, premios, mejoras o beneficio).
- Ejemplo para llegar al nivel 2: ~5 apoyos de 3 € y ~2 de 5 € (o combinaciones parecidas).
- Las plataformas se quedan una comisión (Patreon y Discord se llevan bastante más que Ko-fi): hay que tenerla en cuenta al fijar precios.
- Si el beneficio crece, revisar las obligaciones fiscales (en España, los ingresos de este tipo también se declaran).

- Modelo recomendado: **suscripción de apoyo recurrente** (Ko-fi, Patreon o suscripciones de servidor de Discord) con recompensas cosméticas o sociales, más donaciones puntuales.

## 3b. Restricciones a tener en cuenta para el negocio

Las **Minecraft Usage Guidelines / EULA de Mojang** limitan cómo se puede monetizar un servidor (conviene revisar la versión vigente):
- Se puede cobrar por **cosméticos** y aceptar **donaciones**, pero no vender **ventajas de juego** (pay-to-win: ítems, recursos, poder, etc.).
- Todos los jugadores deben pagar el mismo precio por lo mismo.
- La marca no puede dar a entender que Mojang o Microsoft la respaldan ni usar "Minecraft" como parte del nombre de la marca.
- Para un SMP Vanilla, encaja bien de por sí: lo que se puede monetizar es la comunidad, los cosméticos y el contenido, no el juego.

## 4. Tareas / pendientes

- [x] Explicar el proyecto (sección 2).
- [ ] Definir la identidad de marca (tono, público, propuesta de valor).
- [ ] Definir la estrategia de redes sociales.
- [ ] Esbozar el plan de negocio / monetización.
- [ ] Clonar / adjuntar el repositorio real cuando el usuario tenga acceso al PC.
- [ ] Compartir el repositorio de AmberBot.
- [ ] Adjuntar este documento al nuevo proyecto.

## 5. Registro cronológico de la conversación

### 2026-11-24
- El usuario explica la situación: necesita trabajar sobre un repositorio que está en su PC, pero no está en casa.
- Se acuerda usar este chat como provisional y documentar todo en este `.md`.
- Se crea este documento y se sube a la rama de trabajo.
- El usuario resume el proyecto: AMBERGATES SMP (ver sección 2). Pide centrar esta sesión en marca, redes y plan de negocio, no en lo técnico.
- Se apuntan las restricciones de la EULA de Mojang que afectan a la monetización (sección 3b).
- Objetivo definido: hobby que se pague solo con algo de beneficio extra. Se propone un modelo de apoyo recurrente con recompensas cosméticas o sociales.
- Costes: PebbleHost ~9 €/mes y Railway 5 USD/mes (acumulable). Total ~13,5 €/mes. Se fijan objetivos de 15 € (cubierto) y 25 € (con margen).

## 6. Notas para el asistente del proyecto definitivo

- Leer este documento entero antes de empezar.
- Lo que aquí figure como "decisión tomada" ya está acordado con el usuario; no volver a plantearlo salvo que el código real lo contradiga.
- Si algo de este documento no encaja con el repositorio real, priorizar el código y avisar al usuario.
