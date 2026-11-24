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

## 3a. Marca y redes

- **Público objetivo:** toda Europa (no solo España).
  - Implicación: el **inglés** debería ser el idioma principal (servidor, Discord, redes), con canales o contenido en otros idiomas (p. ej. español) como complemento.
  - La zona horaria de referencia es Europa central (CET), útil para fijar eventos y horas de publicación.
- **Idioma actual:** todo en inglés (TikTok, textos). Encaja con el público europeo.
- **Staff:** solo el usuario. Claude hace de apoyo en estrategia, contenido y programación. **El tiempo es el recurso más escaso**, así que hay que priorizar lo que se pueda automatizar (AmberBot, publicaciones programadas).
- **Logo:** `<A>` / `<AMBERGATES>` con tipografía de bloques en 3D, degradado de amarillo a naranja ámbar y sombra en rojo oscuro o granate, con chevrons `< >` a los lados. Funciona bien a tamaño pequeño (el icono `<A>`) y casa con el nombre.
  - **Paleta de marca deducida:** amarillo ámbar, naranja, rojo oscuro o granate y fondos oscuros.
- **Redes sociales:** capturas guardadas en `docs/capturas/`.

### Análisis de TikTok @ambergates_smp (2026-11-24)
- Bio: "Minecraft 26.2 Vanilla SMP server. (Java) IP at our DISCORD ⬇️" + enlace de invitación a Discord. Historia destacada "IP" con la invitación.
- Métricas: **53 seguidores, 341 seguidos, 44 me gusta**. Unos 20 vídeos publicados y varios programados (27/11, 26/11…).
- Visualizaciones: un vídeo **fijado con 15,8 mil**; los primeros rondan las 640–650 y bajan con el tiempo hasta 77–275 en los más recientes.
- Todos los vídeos usan la **misma plantilla**: un clip de gameplay con el logo grande en el centro y el texto "Minecraft Vanilla SMP Server [Java] [26.2] [FREE access 24/7] Ip in the comments / Ip at comments".

**Diagnóstico:**
1. Los vídeos son **anuncios, no contenido**: el mismo mensaje una y otra vez. El algoritmo y la audiencia se cansan, y por eso bajan las visualizaciones.
2. La interacción es muy baja (44 me gusta en unas 20.000 visualizaciones): nadie tiene un motivo para dar me gusta, comentar o seguir.
3. **La llamada a la acción no es coherente:** los vídeos dicen "IP in the comments" y la bio dice "IP at our Discord".
4. Seguir a mucha más gente de la que te sigue (341 frente a 53) da imagen de follow-for-follow.
5. El texto grande en el centro tapa el gameplay, que es lo que engancha.
6. Lo positivo: la marca visual es **coherente y reconocible** y el inglés es el idioma correcto.
7. **Corrección:** el vídeo de 15,8 mil fue una **promoción pagada** (TikTok Promote), no alcance orgánico. El alcance orgánico real está entre 77 y 650 visualizaciones por vídeo y va a la baja.

**Sobre la publicidad pagada:**
- Antes de volver a pagar, medir cuánto costó cada miembro nuevo de Discord: coste de la promoción ÷ entradas a Discord atribuibles.
- Promocionar un vídeo-anuncio poco atractivo da visualizaciones pero pocas conversiones. Si se vuelve a pagar, que sea sobre un vídeo de contenido que ya haya funcionado bien de forma orgánica.
- Con un objetivo de autofinanciación (~13,5 €/mes de costes), el gasto en anuncios tiene que estar muy controlado. Prioridad: contenido orgánico; anuncios solo como acelerador puntual.

## 3c. Discord: estado actual (2026-11-24)

> Las capturas de Discord **no** se guardan en el repo porque muestran nombres y estados de otros miembros. Aquí solo se resume lo que se ve.

- **Miembros:** 52 en total (no 30), con unos 12–17 conectados. Servidor con la función de "Comunidad" de Discord activada.
- **Flujo de entrada (funciona bien):**
  1. Preguntas de presentación (onboarding de Discord).
  2. Canal `#welcome`: AmberBot muestra un mensaje "Join in seconds" con los botones **Link Minecraft account** y **Check my access**.
  3. Al vincular, AmberBot asigna el usuario de Discord a su cuenta de Minecraft Java y lo **añade automáticamente a la whitelist** por RCON. No hace falta que el staff apruebe nada.
- **Estructura de canales actual:**
  - `#welcome`
  - **Server-info:** `#server-ip`, `#smp-rules`
  - **Text Channels:** `#general`, `#anouncements` (sic), `#suggestions`. Están bloqueados hasta que el usuario se verifica.
  - **Voice Channels:** `room-1` … `room-4` (algunos con límite de 4 o 6 personas)
- **Observaciones:**
  1. `#general` está lleno de **mensajes automáticos de "X se ha unido"** y casi no hay conversación. Da sensación de servidor vacío.
  2. **Errata:** `anouncements` → `announcements`.
  3. El mensaje de bienvenida menciona `#rules`, pero el canal se llama `#smp-rules`. Hay que comprobar que el enlace funciona.
  4. **Posible abandono en la entrada:** en la lista de miembros de `#general` (canal bloqueado) aparecen unas 32 personas, contando a AmberBot, de 52. Si `#general` solo lo ven los verificados, **unas 20 personas entraron y no terminaron de vincular su cuenta**. Está pendiente confirmarlo.
  5. Faltan canales para lo que define la comunidad: construcciones y capturas, proyectos comunitarios, chat del juego, eventos. Tampoco se ven roles con identidad propia.
  6. Varios miembros llevan la **etiqueta de servidor** (server tag) de otros servidores de Minecraft (por ejemplo DSMP, LC). Una etiqueta propia de Ambergates sería publicidad gratuita; requiere mejoras (boosts) del servidor.
  7. Los nombres de los canales de voz (`room-1…4`) son genéricos: es una oportunidad para darles personalidad de marca.

### Teoría del usuario sobre la fuga en la verificación
- **Hipótesis:** muchos de los que no terminan de vincular la cuenta tienen **Minecraft no premium** (sin licencia original de Java). El servidor comprueba las cuentas premium, así que no pueden entrar.
- **Indicio a favor:** en las capturas se ve a un miembro jugando con **SKlauncher**, un launcher muy usado por jugadores no premium.
- **Pendiente:** confirmar con datos (p. ej. si AmberBot registra los intentos de vinculación fallidos y su motivo). Hay que tener en cuenta que admitir cuentas no premium tiene implicaciones de seguridad y de cumplimiento de la EULA; se tratará cuando el usuario quiera.

### Propuesta de estructura (pocos canales, todo en inglés)
> ⚠️ **Sugerencias sin aprobar.** El usuario mandó las capturas solo para dar contexto del estado actual y prefiere dejar las sugerencias para más adelante. No aplicar nada sin consultarle.

Con unos 30 usuarios activos, **demasiados canales dispersan la actividad**. Propuesta:
- **📌 START HERE:** `#welcome` (verificación), `#rules`, `#how-to-join` (IP y pasos), `#announcements`
- **💬 COMMUNITY:** `#general`, `#showcase` (capturas y construcciones), `#suggestions`
- **⛏️ SMP:** `#projects` (canal foro: un hilo por proyecto comunitario o granja), `#ingame-chat` (puente con el juego, si se hace)
- **🔊 VOICE:** 2–3 canales con nombres temáticos (p. ej. `Overworld`, `Nether`, `The End`)
- **Más adelante:** `#support-the-server` (Ko-fi y barra de objetivo mensual)
- Mover los mensajes de bienvenida del sistema fuera de `#general` (a `#welcome` o desactivarlos).

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
- Público objetivo: toda Europa. Ya existe un logo y hay pruebas en redes (TikTok @ambergates_smp). No se pudo acceder al perfil desde la nube.
- El usuario manda capturas de TikTok (guardadas en `docs/capturas/`). Se analizan el perfil y el logo (sección 3a). Staff: solo el usuario, con Claude como apoyo.
- Se aclara que el vídeo de 15,8 mil fue una promoción pagada. El usuario pide aparcar el tema de las redes y pasar a revisar su servidor de Discord con capturas.
- Revisión de Discord (sección 3c): 52 miembros. Whitelist automática al vincular la cuenta de Java con AmberBot por RCON. Se detectan un `#general` lleno de mensajes de entrada, una errata, un posible abandono en la verificación y que faltan canales de comunidad. Se propone una estructura nueva.
- El usuario aclara que las capturas eran **solo de contexto**. Las sugerencias sobre Discord quedan aparcadas para más adelante. Preferencia: mientras da contexto, **escuchar y registrar sin proponer cambios** salvo que lo pida.
- Teoría del usuario: la fuga en la verificación se debe a jugadores con Minecraft no premium (sección 3c).

## 6. Notas para el asistente del proyecto definitivo

- Leer este documento entero antes de empezar.
- Lo que aquí figure como "decisión tomada" ya está acordado con el usuario; no volver a plantearlo salvo que el código real lo contradiga.
- Si algo de este documento no encaja con el repositorio real, priorizar el código y avisar al usuario.
