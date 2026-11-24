# AmberGates SMP · estado (datos a 2026-11-24)

## 0. Decisiones del usuario (no se vuelven a discutir)
| Ámbito | Decisión |
|---|---|
| Objetivo | Hobby que se pague solo y deje algo de beneficio. Sin escalar ni vivir de ello. |
| Público | Europa. |
| Admisión | **Solo cuentas premium**. **Vínculo obligatorio DC ↔ usuario de MC en la whitelist**: cualquier cambio en la admisión debe respetarlo. |
| Marketing | Promoción pagada de TT: fracaso, **no se analiza** salvo que lo pida el usuario. Nueva estrategia **desde el 28 nov**. Vídeos aprobados: D2, D3, J1, H3. Calendario aprobado. Ver `marketing/plan-contenido.md`. |
| Forma de trabajar | Claude organiza; los subroles los crea el usuario. No adelantarse. Lo técnico, solo si se pide (foco en marca, redes y negocio). Las ideas sobre DC están aparcadas (las capturas eran solo de contexto). Documentación según `GUIA_ESCRITURA.md`. |

## 1. Resumen
- SMP de MC **Java 26.2 Vanilla**: comunidad técnica y de construcción, casual, con proyectos comunitarios (granjas). Ya está lanzado.
- Idioma público EN · zona horaria CET · equipo: el usuario solo, con Claude de apoyo. El tiempo es lo más escaso, así que se automatiza.
- Este repo (`oddchunks-ctrl/Claude`, rama `claude/project-context-documentation-q9yr6t`) es el contexto provisional creado en la nube.
- El proyecto real (hecho con Codex) está en el PC. AB está en el repo privado `oddchunks-ctrl/amberbot`.
- La nube bloquea TT, YT y DC: se trabaja con capturas del usuario.

## 2. Técnico (resumen)
- **Servidor:** Fabric + Lithium; se entra con cliente Vanilla sin mods · PebbleHost 8 GB · whitelist activa · RCON con DC · algunos datapacks que no alteran el Vanilla (sin detallar).
- **Mods propios** (código en el PC):
  - *Rangos*: rangos sincronizados con DC.
  - *Statistics*: estadísticas y ascensos.
  - *Propiedades*: claims por chunks, `/trust` e `/inspect` (30 días).
- **AB v0.8.0:**
  - Node 22 · discord.js 14.22.1 · SQLite en `/data` · Railway EU West · despliegue automático desde `codex/main` · tests y CI.
  - Funciones: admisión (§4), `!ip`, sugerencias en hilos privados, anuncios de ascensos en `#general`, sincronización de roles DC ↔ MC.
  - Registra los eventos `admission_link_failed` y `minecraft_profile_lookup` con su causa (sirven para medir la fuga).
  - Su README remite a documentos del PC que no están en el repo: `ESTADO_PROYECTO.md`, `discord.md`, `HOSTING.md`, `REGLAS_SERVIDOR.md`, `Rangos-fabric/`.

## 3. Economía
- **Costes:** PebbleHost ~9 €/mes + Railway 5 USD (~4,5 €; el saldo que sobra se acumula) = **~13,5 €/mes (~160 €/año)**.
- **Objetivos:** ~15 €/mes cubre costes · ~25 €/mes con margen (p. ej. 5 apoyos de 3 € y 2 de 5 €).
- **Modelo (no aprobado):**
  - Suscripción recurrente de 2–3 niveles + donaciones, en Ko-fi (menos comisión que Patreon o DC).
  - Recompensas sociales o cosméticas compatibles con Vanilla: rol y color en DC, etiqueta en el chat, muro de agradecimientos, cabezas, partículas del servidor, votar el próximo proyecto.
  - Barra "% del mes cubierto" mostrada por AB.
- **No hacer:** P2W · pagar por jugar · nada que divida a quienes pagan de quienes no.
- **Supporter:** el rol ya existe (internamente `patreon`). Falta saber cómo se cobra y qué recibe.
- **Si hay beneficio:** se declara en España.
- **EULA de Mojang:** cosméticos y donaciones sí; ventajas de juego no · mismo precio para todos · sin "Minecraft" en la marca ni dar a entender respaldo de Mojang o Microsoft.
- ⚠️ **Supporter da 32 chunks protegidos frente a 20.** Si va ligado a pagar, es posible P2W. Revisar antes de monetizar. Choca con cualquier mensaje de "no P2W".

## 4. DC y admisión
- **Datos:** 52 miembros, ~12–17 conectados, función de Comunidad activada.
- **Canales:** `#welcome` · Server-info: `#server-ip`, `#smp-rules` · Text (bloqueados hasta la admisión): `#general`, `#anouncements` (sic), `#suggestions` · voz: `room-1…4`.
- **Admisión:**
  1. Onboarding nativo de 3 tarjetas EN ("Sounds good" → "Let's build together" → "Ready to link"). Hasta entonces solo se ven `#welcome` y `#rules`.
  2. Botones **Link Minecraft account** / **Check my access**.
  3. API de Mojang → UUID (sin comprobar que la cuenta sea del usuario).
  4. Rol Member → `whitelist add` por RCON → se muestra la IP. Todo automático.
- **Roles:**
  - Member `#C7C2B8` → Honored `#D99545` (automático: 4096 bloques, 600 monstruos y 7 días con ≥30 min) → Elite `#FF5555` (manual). Los tres son excluyentes.
  - Supporter `#F0CC6B` y MOD `#57B86B` se combinan con cualquiera.
- **Fuga:**
  - ~32 de 52 miembros ven `#general`, así que ~20 no terminaron la admisión (sin confirmar).
  - Causa: jugadores no premium (teoría del usuario; un miembro usa SKlauncher). Se acepta por la decisión "solo premium".
  - Caso que se escapa: un no premium que escribe el nombre de alguien premium pasa la admisión y entra en la whitelist sin poder jugar, y además se queda con el nombre de otro.
- **Observaciones:**
  - `#general` está lleno de mensajes de "X se ha unido" y parece vacío.
  - Errata en `anouncements`.
  - La bienvenida enlaza a `#rules`, pero el canal es `#smp-rules`: comprobar el enlace.
  - Faltan canales de construcciones, proyectos y eventos. Voz con nombres genéricos.
  - Hay miembros con la etiqueta de otros servidores (DSMP…).
- **Sin acceso manual a DC.** Alternativa: leerlo con el token de AB, añadido de forma segura y nunca pegado en el chat.

## 5. Normas y lore (`config/rules.en.md` de AB)
- **9 normas:** respetar el trabajo ajeno · claims y `/trust` · zonas comunitarias del staff · PvP solo si ambos aceptan · borde de 5.000 bloques que crece con la comunidad · sin trampas ni saltarse protecciones · cuidar el rendimiento · conflictos con `/inspect` y el staff, sin represalias · baneos temporales o permanentes.
- **El End está cerrado hasta derrotar al dragón todos juntos** (fecha por decidir).
- El lore (borde que crece y evento del dragón) es buen material de marca y de contenido.

## 6. Marca
- AmberGates SMP · bot AmberBot.
- **Logo:** `<A>` / `<AMBERGATES>` en bloques 3D, degradado de amarillo a naranja ámbar, sombra granate y chevrons `< >`. Funciona en pequeño.
- **Paleta:** ámbar · naranja · granate · fondos oscuros, más los colores de los roles (§4).
- **Posicionamiento:** "Peaceful, cooperative, casual technical Minecraft 26.2 Vanilla. No client mods required." / "Build, farm and create together."

## 7. Pendientes
- [ ] ⚠️ Hacer privado el repo `oddchunks-ctrl/Claude` (ahora es público; lo hace el usuario).
- [ ] Mejorar la admisión para reducir la fuga, respetando el vínculo DC ↔ MC.
- [ ] Medir la fuga con la SQLite de AB.
- [ ] Revisar el bonus de chunks de Supporter (EULA).
- [ ] Monetización: plataforma, niveles y recompensas de Supporter; consumo real de Railway.
- [ ] Marca: propuesta de valor en una frase, tono de voz y guía breve.
- [ ] Traer al proyecto definitivo los documentos y mods del PC.
- [ ] YT: revisar el canal (aparcado; bloqueado desde la nube).

## 8. Ideas aparcadas para DC (no aprobadas)
- **Estructura EN:**
  - START HERE: `#welcome`, `#rules`, `#how-to-join`, `#announcements`
  - COMMUNITY: `#general`, `#showcase`, `#suggestions`
  - SMP: `#projects` (foro), `#ingame-chat`
  - Voz: Overworld / Nether / The End
  - Más adelante: `#support-the-server`
- **Ajustes:** sacar los mensajes de entrada de `#general` · corregir la errata · etiqueta de servidor propia (requiere boosts) · mensaje privado a quien no termine de vincular.
