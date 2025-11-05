# PROMPTS para agente Full Stack – Vendilio

Este archivo define prompts reutilizables para un agente de IA full stack encargado de diseñar y desarrollar Vendilio (frontend + backend), considerando flujos básicos, alternos y de excepción.

---

## 1. Prompt de sistema (contexto base)

Úsalo como “System Prompt” o como prompt base para el agente.

> **Prompt:**
>
> Eres un desarrollador full stack senior especializado en arquitectura de aplicaciones móviles y backend para productos tipo marketplace y subastas entre particulares. Tu tarea es ayudarme a diseñar y desarrollar Vendilio, una app móvil de subastas de artículos de segunda mano basada en invitaciones.
>
> Siempre debes:
> - Leer y tomar como verdad principal el archivo `context/CONTEXT.md` del repositorio. Si algo no está definido ahí, trátalo como **pendiente / decisión abierta**, no como un requisito ya aprobado.
> - Explicitar supuestos cuando tengas que proponer algo no definido y marcarlos como "SUPUESTO" y "PENDIENTE DE VALIDAR".
> - Proponer soluciones pensando en escalabilidad, seguridad y buena experiencia de usuario.
> - Incluir en tus respuestas:
>   - Flujos **básicos**.
>   - Flujos **alternos**.
>   - Flujos de **error / edge cases** (por ejemplo: errores de red, datos inconsistentes, estados no válidos, etc.).
> - Sugerir nombres claros para endpoints, entidades y componentes, en inglés para el código y en español para la UX cuando aplique.
> - Producir respuestas estructuradas, usando secciones y listas.
>
> Evita inventar features que no estén alineadas con `CONTEXT.md`. Si crees que una funcionalidad adicional es necesaria, propónla pero márcala explícitamente como idea y no como requerimiento confirmado.

---

## 2. Prompt – Definir arquitectura y stack inicial

> **Prompt:**
>
> Toma el archivo `context/CONTEXT.md` como referencia y propón una arquitectura técnica para Vendilio.
>
> Quiero que definas:
> 1. **Stack sugerido**:
>    - Frontend (app móvil): propone una opción (por ejemplo, React Native, Flutter, etc.) y justifica brevemente.
>    - Backend (framework y lenguaje).
>    - Base de datos (SQL o NoSQL) y justificación.
>    - Manejo de autenticación (tokens, refresh tokens, etc.).
> 2. **Módulos backend**:
>    - Servicios necesarios (Auth, Users, Auctions, Bids, Invitations, Chat, Ratings, Penalties, etc.).
>    - Principales endpoints REST o GraphQL, con ejemplos de rutas y payloads.
> 3. **Modelado de datos**:
>    - Lista de entidades principales y sus campos (User, Auction, Bid, Invitation, ChatMessage, Rating, Penalty, etc.).
>    - Relaciones entre entidades.
> 4. **Flujos críticos**:
>    - Crear subasta.
>    - Participar en subasta (bid).
>    - Cierre de subasta con selección de ganador.
>    - Confirmación/rechazo de compra y aplicación de penalización.
>
> Asegúrate de contemplar flujos básicos, alternos y de excepción en cada parte. Marca los puntos que dependan de decisiones pendientes como "PENDIENTE DE DEFINIR".

---

## 3. Prompt – Implementación del módulo de Acceso (Auth)

> **Prompt:**
>
> A partir del `context/CONTEXT.md`, diseña e implementa el **módulo de autenticación (Auth)** para Vendilio.
>
> Necesito:
> 1. **Modelos de datos** mínimos relacionados con usuarios y sesiones.
> 2. **Endpoints** para:
>    - Sign Up (registro de usuario).
>    - Login (inicio de sesión).
>    - Recuperación de contraseña (solicitar y resetear).
>    - Cierre de sesión (logout) y expiración de token.
> 3. **Validaciones**:
>    - Formato de email.
>    - Fortaleza de contraseña.
>    - Manejo de usuarios suspendidos o con penalizaciones (cuando aplique).
> 4. **Edge cases**:
>    - Intentos fallidos de login repetidos.
>    - Tokens expirados.
>    - Recuperación de contraseña con enlaces o códigos expirados o ya usados.
> 5. **Ejemplos de código**:
>    - Definición de modelos.
>    - Handlers/controladores de endpoints.
>    - Middlewares para proteger rutas autenticadas.
>
> Usa nombres claros en inglés para el código. Señala explícitamente cómo manejarías los errores a nivel API (códigos HTTP y estructura de respuesta).

---

## 4. Prompt – Implementación del módulo “Mis Subastas” (Vendedor)

> **Prompt:**
>
> Usando el documento `context/CONTEXT.md`, diseña e implementa el **módulo de “Mis Subastas” para el vendedor**.
>
> Necesito que definas y/o generes:
> 1. **Modelos de datos** relacionados:
>    - Auction (subasta).
>    - AuctionItem / Item (si lo separas).
>    - Invitation (invitaciones).
>    - AuctionStatus, etc.
> 2. **Endpoints backend** para:
>    - Crear nueva subasta.
>    - Guardar subasta como borrador.
>    - Publicar subasta.
>    - Listar subastas del vendedor (activas, cerradas, borradores).
>    - Reactivar subasta (considerando la restricción de 24 horas).
>    - Gestionar invitados (agregar, remover, revocar).
> 3. **Reglas de negocio clave**:
>    - Diferencia entre subasta privada y abierta.
>    - Límite de profundidad de invitaciones (invitar contactos de contactos solo un nivel).
>    - Manejo de estados: Programada, Activa, Cerrada con ofertas, Cerrada sin ofertas, Reactivada.
> 4. **Flujos**:
>    - Flujo básico de creación y publicación de subasta.
>    - Flujo alterno de borrador.
>    - Flujo de reactivación.
>    - Edge cases (errores al subir fotos, duraciones inválidas, vendedor con restricciones, etc.).
> 5. **Propuesta de interfaz frontend**:
>    - Estructura de pantallas o componentes para:
>      - Lista de subastas del vendedor.
>      - Formulario de nueva subasta.
>      - Detalle de subasta en modo vendedor.
>
> Incluye ejemplos de endpoints (URL, método, body, responses) y, si es posible, fragmentos de código de controladores y componentes.

---

## 5. Prompt – Implementación del módulo Comprador

> **Prompt:**
>
> Con base en `context/CONTEXT.md`, diseña e implementa el **módulo de Comprador**.
>
> Necesito:
> 1. **Modelos de datos adicionales** si se requieren (por ejemplo, Bid, Penalty, Rating).
> 2. **Endpoints backend** para:
>    - Listar invitaciones a subastas del comprador.
>    - Aceptar/rechazar invitación.
>    - Invitar contactos (cuando la subasta sea abierta y lo permita).
>    - Ver subasta activa (datos relevantes para comprador).
>    - Enviar pujas (bids) con incrementos predefinidos.
>    - Enviar preguntas al vendedor.
>    - Confirmar o rechazar la compra cuando tiene la puja más alta.
>    - Consultar historial de participación y compras.
> 3. **Reglas de negocio y edge cases**:
>    - Aplicación de penalización de 24 horas cuando rechaza compra siendo ganador o no responde en el tiempo definido.
>    - Impedir participación en subastas cuando hay penalización activa.
>    - Manejo de empates de pujas.
>    - Manejo de condiciones de carrera (dos pujas casi simultáneas).
> 4. **Flujos de UI**:
>    - Pantalla de invitaciones a subastas.
>    - Pantalla de subasta activa (lista de participantes, puja actual, botones de +$10, +$20, +$50, +$100, preguntas).
>    - Pantalla de confirmación de compra tras cierre.
>    - Pantalla de historial de subastas del comprador.
>
> Entrega la definición de endpoints, contratos de datos (request/response) y propuesta de componentes/pantallas para el frontend.

---

## 6. Prompt – Chat, entrega y calificaciones

> **Prompt:**
>
> A partir del contexto de `CONTEXT.md`, diseña e implementa la funcionalidad de:
>
> - Chat entre comprador y vendedor tras confirmación de compra.
> - Confirmación de entrega.
> - Calificación mutua (vendedor → comprador, comprador → vendedor).
>
> Especifica:
> 1. **Entidades y modelos**:
>    - ChatThread / Conversation.
>    - ChatMessage.
>    - Rating.
> 2. **Endpoints**:
>    - Crear un chat cuando se confirma una venta.
>    - Enviar y recibir mensajes.
>    - Marcar entrega como realizada (por vendedor).
>    - Confirmar recepción de producto (por comprador).
>    - Enviar calificaciones.
> 3. **Reglas de negocio**:
>    - En qué momento exacto se abre el chat.
>    - Qué ocurre si una de las partes cancela.
>    - Cómo se registran las calificaciones para uso futuro (score promedio, número de transacciones, etc.).
> 4. **Edge cases**:
>    - Una de las partes no responde en el chat.
>    - Discrepancia entre “entregado” vs “no recibido”.
>    - Posible futuro flujo de soporte/mediación (marcar solo como "por definir" sin implementarlo completamente).
>
> Proporciona ejemplos de estructuras de datos y respuestas JSON.

---

## 7. Prompt – Pruebas, validaciones y manejo de errores

> **Prompt:**
>
> Considerando todos los módulos definidos en `CONTEXT.md` (Auth, Mis Subastas, Comprador, Chat, Penalizaciones, etc.), propón una estrategia de:
>
> 1. **Validación de datos en backend**:
>    - Ejemplos de validaciones por entidad.
>    - Mensajes de error consistentes.
> 2. **Manejo de errores**:
>    - Estructura estándar de respuestas de error API (códigos HTTP, cuerpos de respuesta).
>    - Manejo de errores de red y timeouts.
> 3. **Pruebas automáticas**:
>    - Tipos de tests recomendados (unitarias, integración, end-to-end).
>    - Ejemplos de casos de prueba para:
>      - Creación de subasta.
>      - Pujas concurrentes.
>      - Cierre de subasta y selección de ganador.
>      - Aplicación de penalización de 24 horas.
>
> Asegúrate de listar casos felices, casos alternos y edge cases.

