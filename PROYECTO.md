# AmberGates SMP — estado del proyecto
> Hechos a fecha **2026-11-24**. Las decisiones están en `DECISIONES.md`; el marketing en `marketing/README.md`.

## 1. Resumen
- **Qué es:** SMP de Minecraft **Java 26.2 Vanilla**. Comunidad técnica y de construcción, de ambiente casual, con proyectos comunitarios (granjas…). Ya está lanzado.
- **Objetivo:** hobby que se pague solo y deje algo de beneficio.
- **Público:** Europa; idioma público en inglés; zona horaria de referencia CET.
- **Equipo:** solo el usuario, con Claude de apoyo. El tiempo es el recurso más escaso, así que se prioriza lo que se pueda automatizar.
- **Repositorios y documentos:**
  - Este repo (`oddchunks-ctrl/Claude`, rama `claude/project-context-documentation-q9yr6t`) es el contexto provisional, creado en la nube.
  - El proyecto real (hecho con Codex) está en el PC del usuario.
  - Bot: repo privado `oddchunks-ctrl/amberbot`.
- **Límites del entorno en la nube:** la red bloquea TikTok, YouTube y Discord, así que se trabaja con capturas del usuario.

## 2. Técnico (solo resumen; no se profundiza si el usuario no lo pide)
- **Servidor:**
  - Fabric + Lithium; se entra con el cliente Vanilla, sin mods.
  - PebbleHost, 8 GB. Whitelist activa. Conectado a Discord por RCON.
  - Algunos datapacks que no alteran el Vanilla (sin detallar).
- **Mods propios:**
  - *Rangos*: rangos sincronizados con Discord.
  - *Statistics*: estadísticas y ascensos.
  - *Propiedades*: protecciones por chunks, `/trust` e `/inspect` (30 días de historial).
  - El código está en el PC.
- **AmberBot** (v0.8.0; Node 22, discord.js 14.22.1, SQLite en `/data`):
  - Railway, EU West. Despliegue automático desde la rama `codex/main`. Tiene tests y CI.
  - Su README es un registro largo que remite a documentos del PC que no están en el repo: `ESTADO_PROYECTO.md`, `discord.md`, `HOSTING.md`, `REGLAS_SERVIDOR.md`, `Rangos-fabric/`.
  - Funciones: onboarding y admisión (ver §4), comando `!ip`, sugerencias en hilos privados, anuncios de ascensos en `#general` y sincronización de roles Discord ↔ Minecraft.
  - Registra los eventos `admission_link_failed` y `minecraft_profile_lookup` con su causa, útiles para medir la fuga.

## 3. Economía
| Coste | €/mes |
|---|---|
| PebbleHost 8 GB | ~9 |
| Railway (5 USD; el saldo que sobra se acumula) | ~4,5 |
| **Total** | **~13,5 (~160 €/año)** |

- **Objetivos de ingresos:** cubrir costes con ~15 €/mes; con margen, ~25 €/mes (p. ej. 5 apoyos de 3 € y 2 de 5 €).
- **Modelo recomendado (no aprobado):**
  - Suscripción recurrente de apoyo con 2 o 3 niveles, más donaciones.
  - Recompensas sociales o cosméticas compatibles con el cliente Vanilla: rol y color en Discord, etiqueta en el chat, muro de agradecimientos, cabezas, partículas generadas por el servidor, votar el próximo proyecto.
  - Plataforma: Ko-fi, porque cobra menos comisión que Patreon o las suscripciones de Discord.
  - Barra de transparencia ("% del mes cubierto") mostrada por AmberBot.
- **No hacer:** rangos pay-to-win, pagar por poder jugar ni nada que divida a quienes pagan de quienes no.
- **Ya existe el rol Supporter** (internamente `patreon`). Falta saber cómo se cobra hoy y qué recibe exactamente.
- **Fiscalidad:** si hay beneficio, se declara en España.
- **EULA y Usage Guidelines de Mojang:**
  - Se permiten cosméticos y donaciones; no se permite vender ventajas de juego.
  - Mismo precio para todos.
  - No usar "Minecraft" en el nombre de la marca ni dar a entender que Mojang o Microsoft respaldan el servidor.
- ⚠️ **Riesgo:** Supporter da **más chunks protegidos (32 frente a 20)**. Si va ligado a pagar, puede ser una ventaja de juego. Revisarlo antes de monetizar. También choca con un mensaje de "no pay-to-win".

## 4. Discord y admisión
- **Datos:** 52 miembros, unos 12–17 conectados, función de Comunidad activada.
- **Canales:**
  - `#welcome`
  - Server-info: `#server-ip`, `#smp-rules`
  - Text (bloqueados hasta verificarse): `#general`, `#anouncements` (sic), `#suggestions`
  - Voz: `room-1…4`
- **Admisión:**
  1. Onboarding nativo con 3 tarjetas en inglés ("Sounds good", "Let's build together", "Ready to link"). Antes de verificarse solo se ven `#welcome` y `#rules`.
  2. En `#welcome`, "Join in seconds" con los botones **Link Minecraft account** y **Check my access**.
  3. Se busca el nombre en la API de Mojang y se obtiene el UUID. No se comprueba que la cuenta sea del usuario.
  4. Se concede el rol Member y se ejecuta `whitelist add` por RCON.
  5. Solo entonces se muestra la IP. Todo automático, sin aprobación del staff.
- **Roles y colores:**
  - Member `#C7C2B8` → Honored `#D99545` (automático: 4096 bloques, 600 monstruos y 7 días con ≥30 min) → Elite `#FF5555` (manual).
  - Estos tres son excluyentes entre sí. Supporter `#F0CC6B` y MOD `#57B86B` se combinan con ellos.
- **Fuga en la admisión:**
  - Unas 32 personas ven `#general` (bloqueado) de 52 miembros, así que unas 20 no terminaron de verificarse (sin confirmar).
  - **Causa principal: jugadores no premium** (teoría del usuario; un miembro usa SKlauncher). Se acepta como consecuencia de la decisión "solo premium".
  - **Caso que se escapa:** un no premium que escribe el nombre de otra persona con cuenta premium pasa la verificación y entra en la whitelist, pero no puede jugar. Además, así puede quedarse con el nombre de otro.
- **Observaciones:**
  - `#general` está lleno de mensajes automáticos de "X se ha unido" y parece vacío.
  - Errata en `anouncements`.
  - El mensaje de bienvenida remite a `#rules`, pero el canal se llama `#smp-rules`: comprobar el enlace.
  - Faltan canales de construcciones, proyectos y eventos.
  - Los canales de voz tienen nombres genéricos.
  - Varios miembros llevan la etiqueta de otros servidores (p. ej. DSMP).
- No se puede entrar a Discord manualmente. La alternativa es leer el servidor con el token de AmberBot, de forma segura y sin pegarlo en el chat.

## 5. Normas y lore (`config/rules.en.md` de AmberBot)
- **9 normas:**
  1. Respetar el trabajo de los demás.
  2. Usar claims y `/trust`.
  3. Las zonas comunitarias las gestiona el staff.
  4. PvP solo si ambos aceptan.
  5. Borde del mundo de 5.000 bloques que **crece con la comunidad**.
  6. Nada de trampas ni saltarse protecciones.
  7. Cuidar el rendimiento.
  8. Conflictos con `/inspect` y el staff, sin represalias.
  9. Baneos temporales o permanentes.
- **El End está cerrado hasta derrotar al dragón todos juntos** (fecha por decidir).
- El lore (borde creciente y evento del dragón) es buen material de marca y de contenido.

## 6. Marca
- **Nombre:** AmberGates SMP. Bot: AmberBot.
- **Logo:** `<A>` / `<AMBERGATES>`, tipografía de bloques en 3D, degradado de amarillo a naranja ámbar con sombra granate y chevrons `< >`. Funciona bien pequeño.
- **Paleta:** ámbar, naranja, granate y fondos oscuros, más los colores de los roles (§4).
- **Posicionamiento (onboarding):** "Peaceful, cooperative, casual technical Minecraft 26.2 Vanilla. No client mods required." / "Build, farm and create together."
- **Pendiente:** propuesta de valor en una frase, tono de voz y guía de marca breve.

## 7. Pendientes generales
- [ ] Mejorar la admisión para reducir la fuga, **manteniendo el vínculo Discord ↔ Minecraft**.
- [ ] Medir la fuga con la SQLite de AmberBot (`admission_link_failed`, `minecraft_profile_lookup`).
- [ ] Revisar el bonus de chunks de Supporter frente a la EULA.
- [ ] Definir la monetización: plataforma, niveles y recompensas de Supporter. Mirar el consumo real de Railway.
- [ ] Definir la identidad de marca (§6).
- [ ] Traer los documentos del PC y los mods al proyecto definitivo.
- [ ] Revisar el canal de YouTube (bloqueado desde la nube; aparcado).

## 8. Ideas aparcadas (no aprobadas; el usuario pidió dejarlas para más adelante)
- **Discord, estructura mínima en inglés:**
  - START HERE: `#welcome`, `#rules`, `#how-to-join`, `#announcements`
  - COMMUNITY: `#general`, `#showcase`, `#suggestions`
  - SMP: `#projects` (canal de foro), `#ingame-chat`
  - VOICE: Overworld / Nether / The End
  - Más adelante: `#support-the-server`
- **Discord, ajustes:** sacar de `#general` los mensajes de entrada; corregir la errata; etiqueta de servidor propia (requiere boosts); recordatorio por mensaje privado a quien no termine de vincular.
