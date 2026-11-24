# Desarrollo

**Misión:** soporte técnico del resto de roles: AmberBot, mods propios, datapacks y hosting.
Solo se entra en detalles técnicos cuando el usuario lo pide.

## Componentes
- **Servidor de Minecraft:** Java 26.2, Fabric + Lithium, se puede entrar con el cliente Vanilla. Hosting en PebbleHost (8 GB). Whitelist activa.
- **Mods propios:** *Rangos* (rangos sincronizados con Discord), *Statistics* (estadísticas y ascensos), *Propiedades* (protecciones por chunks, `/trust`, `/inspect` con 30 días de historial). El código está en el PC del usuario.
- **Datapacks:** algunos que no alteran la experiencia Vanilla (pendiente de detalle).
- **AmberBot:** repo privado `oddchunks-ctrl/amberbot`, rama `codex/main`, que Railway despliega automáticamente. Versión 0.8.0, Node 22, discord.js, SQLite en `/data`. Resumen completo en `CONTEXTO_PROYECTO.md`, sección 3d.

## Documentos del PC a traer
`ESTADO_PROYECTO.md`, `discord.md`, `HOSTING.md`, `REGLAS_SERVIDOR.md`, `Rangos-fabric/` y los demás mods.

## Pendientes
- [ ] Consultar en la SQLite los fallos de vinculación (`admission_link_failed`, `minecraft_profile_lookup`) para medir la fuga.
- [ ] Localizar dónde se define el bonus de chunks de Supporter (mod *Propiedades* o *Rangos*).
