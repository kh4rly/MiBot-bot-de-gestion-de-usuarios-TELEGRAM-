Para entrar en Mibot: https://t.me/DownDragonBot?start=7_a_Fbnt8hG8ozh4
Teneis un chat disponible directo a mi :)


[README-MIBOT.md](https://github.com/user-attachments/files/32690050/README-MIBOT.md)
# MiBot — Sistema de bots hijo para Telegram

MiBot es el sistema modular de **bots hijo** del bot principal Downdragon. Cada usuario puede crear su propio bot (instancia) con su enlace de invitación, sus usuarios, su grupo de soporte y un panel de gestión `/mibot`. Las funciones disponibles dependen del **plan** contratado y de lo que el **dueño del bot** active en su panel.

---

## Índice

1. [Cómo funciona](#cómo-funciona)
2. [Planes](#planes)
3. [Funciones por sección](#funciones-por-sección)
4. [Toggles del bot (gestión del dueño)](#toggles-del-bot-gestión-del-dueño)
5. [Toggles de plan (barrera de pago)](#toggles-de-plan-barrera-de-pago)
6. [Módulos](#módulos)
7. [Configuración](#configuración)

---

## Cómo funciona

- Un usuario crea su bot con `/mibot` → se le asigna una **instancia** (bot hijo).
- El bot hijo tiene un **enlace de invitación** para que entren sus usuarios: `https://t.me/{bot}?start=bot_{token}`.
- El dueño gestiona todo desde el panel **`/mibot`** (activar/desactivar funciones, usuarios, grupos, peticiones, etc.).
- Los planes los crea y configura el **admin** desde el panel de administración (`/bothijos`): activa los toggles que incluye cada plan.
- Al confirmar un pago, los toggles del plan se aplican automáticamente a la instancia.
- Al expirar un plan de pago, la instancia vuelve al plan **GRATIS** (no se desactiva).
- 3 niveles de toggles: **Defaults** (instancia 0) → **Plan** (`toggles_json`) → **Instancia** (el dueño afina lo suyo).

---

## Planes

Los planes se crean con los botones del panel de administración. Son 4 plantillas base:

| Plan | Uso |
|---|---|
| **GRATIS** | Funciones básicas para probar el sistema |
| **BASICO** | Funciones esenciales |
| **PRO** | Funciones avanzadas |
| **VIP** | Todas las funciones |

> El **admin decide** qué toggles incluye cada plan (no hay valores predefinidos). Cada función numerada de este documento tiene su interruptor en el panel de planes.

Cada plan tiene: nombre, precio, duración en días (0 = ilimitado), descripción, PayPal opcional y sus **toggles de plan**.

---

## Funciones por sección

### 1. 💬 Chat Soporte
El bot hijo funciona como chat de soporte entre el dueño y sus usuarios (con topics).
- Chat habilitado, ver/editar/borrar mensajes, límite de ediciones.
- Admins sin restricciones, títulos con colores, auto-reacciones, historial de ediciones.

### 2. 👥 Ver Clientes Chat
- Ver lista de clientes del chat, recrear chats, banear, ver info de usuario.

### 3. 📋 Gestión de Categorías
- Categorías y peticiones de los usuarios (tickets por categoría).
- Límite de categorías, canales requeridos, límite de peticiones por usuario.

### 4. 📡 Grupo Soporte
- Configurar el grupo de soporte de la instancia.

### 5. 📡 Canales Invitación
- Sistema de invitaciones a canales con paquetes.
- Crear paquete, administrar paquetes, nueva invitación, ver invitaciones activas.
- Límite de paquetes, invitaciones reutilizables, protección por canal requerido, ver usuarios invitados.
- **PayPal**: pago requerido para invitaciones.

### 6.3 🤖 Máx bots por usuario
- Límite de bots que puede crear un usuario.

### 6.4 🚫 DeleteComandos (bloqueo de comandos)
- Bloquear comandos `/` a los usuarios del bot.
- Comandos bloqueados (lista o todos), castigo (nada / borrar / aviso / silenciar / expulsar), minutos de castigo, grupos de comunidad.

### 6.5 🌦 El Tiempo
- Pronóstico por ubicación guardada o por GPS.
- Datos por horas y días: temperatura, sensación, lluvia, viento, ráfagas, humedad, UV, presión, nieve, punto de rocío, visibilidad, evapotranspiración.
- Calidad del aire y pólenes (PM2.5, PM10, ozono, NO₂, abedul, gramíneas, olivo…).
- **Eventos estelares** de 7 días: fases lunares, eclipses, lluvias de meteoros, planetas visibles, horas dorada/azul, pasos de la ISS.
- **Gráfico PNG** del pronóstico.
- **Comparar dos lugares** y búsqueda de ciudad por nombre.
- **Vuelos**: aviones sobrevolando la ubicación en tiempo real (OpenSky), con detalle individual, ruta origen/destino, aerolínea y posición GPS temporal.
- **Resumen matutino automático**: el dueño activa el módulo y cada usuario elige su hora de entrega.
- **Alertas de lluvia**: función de plan de pago.

### 7. 📦 Colecciones
- Botones dinámicos con topics para compartir contenido.
- Máx. colecciones, backup de topics, canales requeridos, mensaje de denegación, restauración, reenvíos, colecciones ocultas con clave.

### 8. 📡 RSS / Feeds
- Fuentes RSS reflejadas en el bot.
- Máx. fuentes, intervalo de refresco, destino oculto de admin, canales de Telegram, ocultar referido.

### 10. 🎮 Pokémon GO
- Módulo Pokémon GO para bots hijo.

### 12. 🔗 Descargas Link
- Descarga de vídeos/audio desde enlaces (YouTube, TikTok, Instagram, X/Twitter, Facebook, Twitch, Reddit, SoundCloud, Spotify, Pinterest, Vimeo, Rumble, Bitchute, Threads, Bluesky…).
- Formatos MP3 y MP4, máx. canales, máx. descargas/día, config por canal, pie personalizado, permitir usuarios, borrar enlace tras descarga, filtro por palabras, playlists completas, sync de userbots.

### 13. 🤖 Userbots
- Habilitar userbots para la instancia.

### 14. 🖼 Galería
- Galería de imágenes/vídeos creada por admins (y usuarios si se permite).
- Límite de elementos, compartir galería, storage en grupo/topic oculto.

### 15. 🎮 Nintendo Switch
- Módulo de Nintendo Switch (Identificacion de los distintos modelos).

### 16. 🔁 Anti-Duplicados
- Control de mensajes repetidos/cruzados en grupos con temas.
- Grupos vigilados añadidos **por enlace de grupo**, ventana de tiempo, similitud (Levenshtein), longitud mínima, avisos con expiración, castigo (nada / silencio / expulsión), ignorar respuestas, topics ignorados.
- Comandos: `/antidup`, `/warns`, `/resetwarns`.

### 17. 🏅 Deportes
- Resultados deportivos en tiempo real y biblioteca histórica.
- **En vivo (hoy)**: LaLiga, Premier League, Champions League, NBA, MLB, NHL, ATP, WTA, WNBA, NWSL y Champions Femenina (fuente: ESPN).
- **Biblioteca por años**:
  - Fútbol: 4 temporadas completas por liga con todos los partidos (football-data.org, key gratuita).
  - F1: temporadas desde 2000 con ganador de cada GP (Jolpi/Ergast).
  - MLB: temporadas desde 2000 con todos los partidos (MLB Stats API).
  - Resto de deportes: catálogo de fechas de los últimos 180 días.
- Detalle por evento: marcador, estado, minuto, estadio, país, temporada y goleadores (cuando la fuente los da).

---

## Toggles del bot (gestión del dueño)

Estos son los interruptores que el **dueño** ve y gestiona en `/mibot`:

| Clave | Función |
|---|---|
| `chat_habilitado` | 1.1 Chat habilitado |
| `chat_ver_ediciones` | 1.2 Ver ediciones |
| `chat_editar_mensajes` | 1.3 Editar mensajes |
| `chat_editar_limite` | 1.3b Límite de ediciones |
| `chat_borrar` | 1.4 Borrar mensajes |
| `chat_admin_sin_restric` | 1.5 Admins sin restricciones |
| `chat_titulos_color` | 1.6 Títulos con colores |
| `chat_auto_reacciones` | 1.7 Auto-reacciones |
| `chat_historial_ediciones` | 1.8 Historial de ediciones |
| `ver_clientes` | 2.1 Ver clientes |
| `ver_recrear_chat` | 2.2 Recrear chat |
| `ver_banear` | 2.3 Banear |
| `ver_info_usuario` | 2.4 Info de usuario |
| `cat_habilitado` | 3.1 Categorías |
| `cat_peticiones` | 3.2 Peticiones pendientes |
| `cat_limite` | 3.3 Límite de categorías |
| `cat_canales_requeridos` | 3.4 Canales requeridos |
| `cat_limite_peticiones` | 3.5 Límite de peticiones |
| `cat_ver_limite_peticiones` | 3.6 Mostrar límite en /mibot |
| `grupo_configurar` | 4.1 Configurar grupo |
| `canales_habilitado` | 5.1 Invitaciones |
| `canales_crear_paquete` | 5.2 Crear paquete |
| `canales_admin_paquetes` | 5.3 Administrar paquetes |
| `canales_nueva_inv` | 5.4 Nueva invitación |
| `canales_ver_inv` | 5.5 Ver invitaciones activas |
| `canales_limite_paq` | 5.6 Límite de paquetes |
| `canales_reutilizable` | 5.7 Invitaciones reutilizables |
| `canales_proteccion` | 5.8 Protección (canal requerido) |
| `canales_ver_usuarios` | 5.9 Ver usuarios invitados |
| `canales_paypal` | 5.9a PayPal (pago requerido) |
| `col_habilitado` | 7.1 Habilitar colecciones |
| `col_max` | 7.2 Máx. colecciones |
| `col_backup` | 7.3 Backup de topics |
| `col_group_id` | 7.4 Grupo oculto (ID) |
| `col_group_extra` | 7.4a Grupo independiente de colecciones |
| `col_channels` | 7.5 Canales requeridos |
| `col_msg` | 7.6 Mensaje denegado |
| `col_restore` | 7.7 Restauración |
| `col_reenvios` | 7.8 Reenvíos |
| `col_reenvios_admin` | 7.9 Solo admins |
| `col_hidden` | 7.9a Colecciones ocultas |
| `col_hidden_pass` | 7.9b Clave de ocultas |
| `rss_habilitado` | 8.0 RSS / Feeds |
| `rss_canales` | 8.0a Reflejar canales |
| `rss_max` | 8.1 Máx. fuentes |
| `rss_intervalo` | 8.2 Refresco |
| `rss_destino_oculto` | 8.3 Destino oculto admin |
| `rss_canales_telegram` | 8.4 Canales Telegram |
| `rss_ocultar_referido` | 8.5 Ocultar referido |
| `pokemon_habilitado` | 10.0 Pokémon GO |
| `descargas_link_enabled` | 12.0 Descargas Link |
| `dl_max_canales` | 12.0b Máx. canales |
| `dl_max_descargas_por_dia` | 12.1 Máx. descargas/día |
| `dl_formatos_mp3` | 12.2a MP3 |
| `dl_formatos_mp4` | 12.2b MP4 |
| `dl_servicios` | 12.3 Servicios |
| `dl_config_canal` | 12.4 Config por canal |
| `dl_pie_enabled` | 12.5 Pie habilitado |
| `dl_pie_descripcion` | 12.5a Pie por defecto |
| `dl_permitir_usuarios` | 12.6 Permitir usuarios |
| `dl_borrar_link` | 12.7 Borrar link tras descarga |
| `dl_filtro_palabras` | 12.8 Filtro por palabras |
| `dl_playlist` | 12.9 Descargar todos los vídeos |
| `dl_userbot_sync` | 12.10 Sync userbots |
| `userbot_habilitado` | 13.0 Userbots |
| `galeria_habilitado` | 14.0 Galería activa |
| `galeria_usuarios` | 14.1 Usuarios crean |
| `galeria_limite` | 14.2 Límite de elementos |
| `galeria_compartir` | 14.3 Compartir galería |
| `galeria_storage` | 14.4 Grupo/topic de copias |
| `nintendo_habilitado` | 15.0 Nintendo Switch |
| `tiempo_habilitado` | 6.5 El Tiempo |
| `tiempo_sin_limite` | 6.5a Sin límite de consultas |
| `tiempo_resumen_auto` | 6.5b Resumen matutino automático |
| `tiempo_resumen_hora` | 6.5c Hora por defecto (0-23) |
| `deportes_activo` | 17.0 Deportes (on/off del dueño) |
| `antidup_activo` | 16.0 Anti-Duplicados (on/off del dueño) |
| `cmd_bloqueo` | 6.4 Bloquear comandos |
| `cmd_bloqueados` | 6.4a Comandos bloqueados |
| `cmd_castigo` | 6.4b Castigo |
| `cmd_castigo_min` | 6.4c Minutos de castigo |
| `cmd_grupos` | 6.4d Grupos de comunidad |

---

## Toggles de plan (barrera de pago)

El **admin** activa estos interruptores en cada plan. Si el plan no los tiene, la sección no aparece en `/mibot`:

| Clave | Función |
|---|---|
| `chat_habilitado` | Chat Soporte |
| `ver_clientes` | Ver clientes |
| `cat_habilitado` | Categorías |
| `grupo_configurar` | Grupo Soporte |
| `canales_habilitado` | Invitaciones |
| `canales_paypal` | Invitaciones con PayPal |
| `col_habilitado` | Colecciones |
| `rss_habilitado` | RSS |
| `pokemon_habilitado` | Pokémon GO |
| `descargas_link_enabled` | Descargas Link |
| `userbot_habilitado` | Userbots |
| `galeria_habilitado` | Galería |
| `nintendo_habilitado` | Nintendo Switch |
| `tiempo_habilitado` | El Tiempo |
| `tiempo_alertas_lluvia` | Alertas de lluvia (pago) |
| `antidup_habilitado` | Anti-Duplicados |
| `deportes_habilitado` | Deportes |
| `gen_max_bots_usuario` | Máx. bots por usuario |
| `cmd_bloqueo` | DeleteComandos (6.4) |

---

## Módulos

| Archivo | Función |
|---|---|
| `modules/mi_bot.py` | Panel `/mibot`, instancias, usuarios, peticiones, pago de planes |
| `modules/admin_modules/bothijos.py` | Panel de administración: planes, toggles, instancias |
| `modules/mi_bot_tiempo.py` | 6.5 El Tiempo (pronóstico, aire, eventos estelares, gráfico, vuelos, alertas) |
| `modules/mi_bot_deportes.py` | 17.0 Deportes (en vivo, biblioteca por años) |
| `modules/mi_bot_antiduplicados.py` | 16.0 Anti-Duplicados |
| `modules/mi_bot_descargas_link.py` | 12.x Descargas Link |
| `modules/mi_bot_galeria.py` | 14.x Galería |
| `modules/mi_bot_nintendo.py` | 15.x Nintendo Switch |
| `modules/mi_bot_rss.py` | 8.x RSS / Feeds |
| `modules/mi_bot_invites.py` | 5.x Canales Invitación |
| `modules/mi_bot_colecciones.py` | 7.x Colecciones |
| `modules/mibot_info.py` | Ayuda de /mibot |
| `data/bot_db.py` | Base de datos (instancias, planes, toggles, catálogos) |

---
