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

## 6. Notas para el asistente del proyecto definitivo

- Leer este documento entero antes de empezar.
- Lo que aquí figure como "decisión tomada" ya está acordado con el usuario; no volver a plantearlo salvo que el código real lo contradiga.
- Si algo de este documento no encaja con el repositorio real, priorizar el código y avisar al usuario.
