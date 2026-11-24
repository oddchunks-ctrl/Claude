# Comunidad

**Misión:** que quien llega se quede, juegue y participe: admisión sin fugas, un Discord vivo y eventos.

## Estado actual (2026-11-24)
- **Discord:** 52 miembros, unos 12–17 conectados, con la función de "Comunidad" activada.
- **Canales:** `#welcome` · Server-info (`#server-ip`, `#smp-rules`) · Text (`#general`, `#anouncements` (sic), `#suggestions`) · Voz (`room-1…4`).
- **Admisión** (la gestiona AmberBot):
  1. Tres tarjetas de onboarding nativo.
  2. En `#welcome`, el botón "Link Minecraft account".
  3. Se busca el nombre en la API de Mojang y se obtiene el UUID.
  4. Se concede el rol Member.
  5. Se añade a la whitelist por RCON.
  6. Se muestra la IP.
- **Roles:** Member → Honored (automático por actividad) → Elite (manual). Supporter y MOD se pueden combinar con ellos.

## Decisiones
- Solo cuentas premium.
- **Vínculo Discord ↔ Minecraft obligatorio** en la whitelist.

## Problema principal: fuga en la admisión
- Unas 32 personas con acceso a `#general` frente a 52 miembros: unas 20 no terminaron la verificación (pendiente de confirmar).
- **Teoría del usuario:** son jugadores no premium. Indicio a favor: un miembro usa SKlauncher.
- Un no premium que escriba el nombre de un jugador premium real pasa la verificación y entra en la whitelist, pero no puede jugar. Además, así puede quedarse con el nombre de otro.
- **Datos disponibles:** AmberBot registra `admission_link_failed` y `minecraft_profile_lookup` (ver `desarrollo/`).

## Pendientes
- [ ] Medir la fuga con los datos de AmberBot.
- [ ] Mejorar el proceso de admisión respetando el vínculo obligatorio.

## Ideas aparcadas (no aprobadas)
- Sacar de `#general` los mensajes automáticos de "X se ha unido".
- Corregir `anouncements` y revisar el enlace a `#rules`.
- Estructura reducida: START HERE / COMMUNITY (`#showcase`) / SMP (`#projects` como foro) / voz con nombres temáticos.
- Etiqueta de servidor propia (requiere boosts).
- Recordatorio por mensaje privado a quien no haya terminado la vinculación.
