# Vendilio – CONTEXT v0.1

## 1. Visión general

Vendilio es una aplicación móvil para subastar artículos de segunda mano entre personas conocidas o conocidas de conocidos, con foco en:

- Subastas pequeñas, privadas o semi-privadas.
- Interacciones basadas en invitaciones.
- Acuerdos de entrega y pago **fuera de la plataforma** (al menos en la primera versión).
- Un sistema simple de reputación (calificaciones entre comprador y vendedor).

Este documento sirve como **contexto funcional** para guiar el diseño de UX, UI y el desarrollo (front y back), así como para alimentar agentes de IA que colaboren en la construcción del sistema.

> Nota: Muchos puntos están marcados como “por definir (TODO)”. Se documentan aquí para futura aclaración, no para que el sistema los implemente de inmediato sin decisión previa.

---

## 2. Glosario de términos

- **Usuario**: Persona registrada en el sistema. Puede actuar como comprador, vendedor o ambos.
- **Vendedor**: Usuario que crea y publica una subasta.
- **Comprador**: Usuario que participa en una subasta pujando por un artículo.
- **Invitado**: Usuario que recibe una invitación para unirse a una subasta.
- **Subasta**: Evento limitado en el tiempo donde se ofrece un artículo con un costo inicial y los compradores realizan pujas.
- **Puja**: Oferta de compra por un importe superior al actual.
- **Subasta privada**: Subasta a la que solo pueden acceder usuarios invitados por el vendedor.
- **Subasta abierta**: Subasta donde los invitados pueden invitar a sus propios contactos, con una profundidad limitada (solo una generación extra).
- **Penalización**: Restricción temporal (ej. 24 horas) que impide a un comprador participar en nuevas subastas si declina la compra tras tener la puja ganadora.
- **Historial**: Listado de subastas en las que el usuario participó como vendedor o comprador.
- **Ubicación**: Estado y municipio donde se realizará la entrega del artículo, y ubicación de entrega acordada (texto libre o puntos predefinidos).

---

## 3. Módulo de Acceso (Auth)

### 3.1 Login

#### Objetivo

Permitir a un usuario acceder a su cuenta de Vendilio de forma segura.

#### Flujo principal

1. El usuario abre la app y selecciona la opción **“Iniciar sesión”**.
2. Ingresa **email** y **contraseña**.
3. El sistema valida credenciales.
4. Si son correctas y la cuenta está activa:
   - Se crea una sesión (token).
   - Se redirige al usuario al **home** (p.ej. “Mis subastas” o “Explorar”, según diseño).

#### Casos alternos

- Usuario intenta iniciar sesión pero:
  - Su cuenta está **pendiente de verificación** (si se agrega verificación por email/telefono → TODO).
  - Su cuenta está **suspendida** (por penalizaciones graves o políticas de uso → TODO).
- Usuario tiene sesión activa en otro dispositivo:
  - Permitir múltiples sesiones o invalidar la anterior → TODO a definir.

#### Edge cases / errores

- Email inválido o contraseña incorrecta:
  - Mostrar mensaje genérico: “Credenciales incorrectas”.
  - Contar intentos fallidos (ej. bloqueo temporal tras X intentos → TODO).
- Email con formato inválido.
- Usuario no encontrado.
- Error de red / servidor:
  - Mostrar mensaje de error.
  - Permitir reintentar.
- Token de sesión expirado:
  - Forzar re-login cuando la API responda 401.

---

### 3.2 Sign Up (Registro)

#### Objetivo

Permitir que nuevos usuarios creen una cuenta para usar Vendilio como compradores y/o vendedores.

#### Flujo principal

1. Usuario selecciona **“Crear cuenta”**.
2. Completa los campos mínimos:
   - Nombre
   - Apellido(s)
   - Email
   - Teléfono (opcional u obligatorio, por definir)
   - Contraseña
   - Acepta Términos y Condiciones y Aviso de Privacidad.
3. El sistema valida:
   - Formato de email.
   - Fortaleza mínima de contraseña.
   - Email no registrado previamente.
4. Se crea la cuenta.
5. Opcionalmente, se envía correo o SMS de verificación (por definir).
6. Usuario es redirigido a la pantalla principal (o a un onboarding breve).

#### Casos alternos

- Email ya existe:
  - Mostrar mensaje y sugerir **“¿Olvidaste tu contraseña?”**.
- Usuario abandona el flujo a la mitad:
  - Se puede guardar parcialmente (draft) o no, según diseño → TODO.

#### Edge cases / errores

- Campos incompletos u obligatorios vacíos.
- Contraseña demasiado débil según reglas configuradas.
- Error de red durante el registro.
- Fallo al enviar correo/SMS de verificación (si aplica).
- Usuario intenta registrarse usando un email temporal o claramente inválido (validaciones por definir).

---

### 3.3 Recuperar contraseña

#### Objetivo

Permitir a un usuario recuperar acceso a su cuenta si olvidó su contraseña.

#### Flujo principal

1. Usuario selecciona **“¿Olvidaste tu contraseña?”** en la pantalla de login.
2. Ingresa su email registrado.
3. El sistema valida que el email exista.
4. Se envía un enlace de recuperación de contraseña o código de verificación (según implementación).
5. El usuario abre el enlace/código:
   - Ingresa nueva contraseña (y confirmación).
   - El sistema actualiza la contraseña y invalida el enlace/código de recuperación.
6. El usuario puede iniciar sesión con su nueva contraseña.

#### Casos alternos

- Email no registrado:
  - Mostrar mensaje genérico (“Si el email existe, enviaremos instrucciones…”).
- Enlace de recuperación expirado:
  - Mostrar mensaje y permitir generar uno nuevo.

#### Edge cases / errores

- Enlace usado más de una vez → debe ser inválido.
- Error de red al solicitar recuperación o al guardar la nueva contraseña.
- Intentos repetidos de recuperación desde la misma IP (posible abuso → TODO).

---

### 3.4 Gestión de sesión y seguridad básica

- Manejo de tokens (JWT o similar).
- Expiración de sesión.
- Posibilidad de cerrar sesión desde la app.
- Protección de endpoints sensibles (subastas, pujas, chat) para usuarios autenticados.

---

## 4. Módulo Vendedor – Mis Subastas

### 4.1 Crear nueva subasta

#### Objetivo

Permitir al vendedor publicar una nueva subasta de un artículo de segunda mano.

#### Datos requeridos para la subasta

- **Artículo**
  - Título / nombre del artículo.
  - Descripción del artículo.
  - Categoría (opcional, pero recomendable → TODO definir categorías).
  - Estado del artículo (nuevo, usado, muy usado… → TODO).
- **Multimedia**
  - Tomar fotos desde la cámara o cargar desde galería.
  - Cantidad mínima y máxima de fotos (ej. 1–10 → TODO).
- **Precio**
  - Costo inicial (precio base desde el que comienzan las pujas).
- **Duración de la subasta**
  - Opción 1 / Opción 2 (aún por definir: podría ser “X horas” o “fecha/hora de inicio y fin”).
  - Validar que la duración mínima y máxima esté en rangos permitidos (ej. mínimo 30 min, máximo 7 días → TODO).
- **Acceso a subasta**
  - Privada.
  - Abierta.
- **Invitados**
  - Subasta privada:
    - Vendedor carga invitados (contactos de familiares, amigos, conocidos).
  - Subasta abierta:
    - Vendedor invita contactos.
    - Estos invitados pueden invitar a sus propios contactos.
    - Invitados de invitados **ya no pueden invitar a más personas** (profundidad máxima = 2).
- **Ubicación**
  - Estado.
  - Municipio.
  - Punto de entrega (texto libre o selección de lugares predefinidos, por definir).
- **Condiciones adicionales**
  - Política de cancelación del vendedor (si decide no vender al final → TODO).
  - Notas para compradores, si aplica.

#### Flujo principal

1. El vendedor ingresa a **“Mis Subastas”** y selecciona **“Nueva subasta”**.
2. Completa datos del artículo, fotos, precio inicial, duración y tipo de acceso.
3. Selecciona ubicación: Estado → Municipio → lugar de entrega.
4. Carga lista de invitados (según tipo de subasta).
5. Revisa resumen de la subasta.
6. Publica la subasta.
7. La subasta queda:
   - En estado **“Programada”** (si inicia en el futuro), o
   - En estado **“Activa”** (si inicia de inmediato).

#### Casos alternos

- Vendedor guarda la subasta como **borrador** y no la publica aún.
- Vendedor edita el borrador antes de publicarlo (cambia descripción, duración, invitados, etc.).
- Vendedor decide **cancelar** la creación antes de publicar.

#### Edge cases / errores

- Campos obligatorios no completados.
- Tipo de acceso inconsistente (ej. subasta marcada como privada pero sin invitados).
- Duración fuera de rangos permitidos.
- Error al subir fotos (formato no permitido, tamaño excesivo).
- Error de red al crear la subasta.
- Vendedor con restricciones (ej. penalización por malas prácticas o reportes → TODO).

---

### 4.2 Invitaciones (vendedor)

#### Subasta privada

- Solo el vendedor puede invitar usuarios.
- Los invitados reciben notificación/invitación a la subasta.
- Cada invitado puede **aceptar** o **rechazar** la invitación.

#### Subasta abierta

- El vendedor invita contactos iniciales.
- Cada invitado que **acepta**:
  - Puede invitar a sus propios contactos.
  - Sus invitados **no pueden** volver a invitar a otros (máximo 2 niveles).
- El vendedor puede:
  - Ver la lista completa de invitados y participantes.
  - **Revocar** invitaciones de usuarios específicos (por razones de confianza, historial, etc.).
  
#### Edge cases / errores

- Invitación enviada a usuario no registrado:
  - El sistema podría permitir registro rápido desde la invitación → TODO.
- Invitación revocada mientras el usuario ya estaba dentro de la subasta:
  - Definir qué ocurre con sus pujas (probablemente invalidarlas y notificar → TODO).
- Límite máximo de invitados por subasta → TODO.

---

### 4.3 Subasta activa (vista del vendedor)

#### Objetivo

Permitir al vendedor gestionar una subasta en curso.

#### Funcionalidad

- Ver datos de la subasta (artículo, fotos, descripción, costo inicial, tiempo restante).
- Ver **lista de compradores participantes** (usuarios que aceptaron la invitación).
- Ver puja actual más alta y su comprador.
- Responder preguntas de posibles compradores (chat o sección de Q&A).
- En subasta abierta:
  - Vendedor puede **no aceptar** a uno o varios compradores invitados.
  - Esto puede implicar:
    - Bloquear su participación en la subasta.
    - Evitar que vean la subasta.
    - Decisión pendiente → TODO.

#### Edge cases / errores

- Compradores expulsados en plena subasta (¿qué pasa si ya pujaron? → TODO).
- Preguntas ofensivas o contenido inapropiado → requerir sistema de reportes / bloqueo → TODO.
- Errores de sincronización en pujas (condiciones de carrera) → manejar desde backend con bloqueos/optimismo.

---

### 4.4 Cierre de subasta (lógica del vendedor)

#### Escenario 1: Subasta termina sin ofertas

- Estado final: **“Cerrada sin ofertas”**.
- El vendedor tiene opción de **reactivar** la subasta:
  - Reactivación permitida a partir de 24 horas después del cierre.
  - Podrá:
    - Mantener los mismos invitados.
    - Ajustar precio, fotos, descripción, duración…
  - Número máximo de reactivaciones → TODO.

#### Escenario 2: Subasta termina con ofertas

1. El sistema identifica la **puja más alta**.
2. Envía solicitud al comprador con puja más alta para **confirmar su interés de compra**.
3. Si el comprador **confirma**:
   - Se considera ganador.
   - Se abre **chat directo** con el vendedor para acordar entrega y pago.
4. Si el comprador **rechaza** (o no responde en cierto tiempo → TODO):
   - El sistema toma la **siguiente puja más alta confirmada**, y repite el proceso.
   - Si ninguna puja resulta confirmada, la subasta se considera **Cerrada sin concreción de venta**.
   - El sistema puede sugerir reactivar subasta u otro manejo.

#### Edge cases / errores

- Empate en pujas (dos compradores con el mismo importe más alto):
  - Podría definirse prioridad por orden de tiempo → TODO.
- Comprador confirma pero luego desaparece / no acude a entrega:
  - Esto impacta calificación y penalizaciones futuras → TODO.
- Vendedor decide no vender a nadie a pesar de pujas válidas:
  - Definir política para evitar abuso → TODO.

---

### 4.5 Chat y entrega (vendedor)

#### Flujo principal

1. Tras la confirmación de compra, se crea un chat entre vendedor y comprador.
2. En el chat acuerdan:
   - Día y hora de entrega.
   - Lugar de entrega (puede cambiar respecto al definido al crear la subasta).
3. Vendedor y comprador pueden modificar el lugar de entrega de común acuerdo.
4. Una vez realizada la entrega:
   - Vendedor marca el artículo como **entregado**.
   - Vendedor califica al comprador (escala y criterios por definir).

#### Edge cases / errores

- Chat no utilizado (se comunican por otro medio).
- Alguna de las partes quiere cancelar el trato tras haber confirmado:
  - Definir impacto en calificaciones y posibles penalizaciones → TODO.
- Problemas de abuso o comportamiento fraudulento → sistema de reportes → TODO.

---

### 4.6 Historial de subastas (vendedor)

- Listado de todas las subastas del usuario como vendedor:
  - Activas.
  - Cerradas (con venta y sin venta).
  - Reactivadas.
- Detalles por subasta:
  - Artículo.
  - Resultado (vendido / no vendido).
  - Comprador final (si lo hubo).
  - Calificación del comprador.
  - Penalizaciones asociadas, si existieron.

---

## 5. Módulo Comprador

### 5.1 Invitaciones a subastas

#### Flujo principal

1. Comprador recibe una invitación a una subasta:
   - Notificación dentro de la app y/o push (por definir).
2. Abre la invitación y ve:
   - Datos de la subasta.
   - Vendedor.
   - Tiempo de inicio y duración.
3. El comprador puede:
   - **Aceptar**.
   - **Rechazar**.

#### Comportamiento según tipo de subasta

- **Subasta privada**:
  - Si acepta:
    - Solo participa él. **No** puede invitar a otros.
- **Subasta abierta**:
  - Si acepta:
    - Puede invitar a sus contactos.
    - Los contactos invitados por él **no pueden** invitar a nadie más.

#### Edge cases / errores

- Comprador con penalización activa de 24 horas:
  - No debería poder aceptar nuevas invitaciones.
  - Mensaje explicando la penalización.
- Invitación expirada (porque la subasta ya terminó o empezó hace mucho):
  - Mostrar mensaje y bloquear acción.

---

### 5.2 Subasta activa (vista del comprador)

#### Funcionalidad

- Ver datos básicos de la subasta:
  - Artículo, descripción, fotos, costo inicial, tiempo restante.
- Ver **lista de compradores participantes** (nombres y/o alias; detalles por definir).
- Ver el importe de la puja actual más alta.
- Realizar pujas mediante botones de incremento:
  - +$10
  - +$20
  - +$50
  - +$100
- Ver su puja actual (si es el máximo postor o no).
- Enviar **preguntas** al vendedor (que se muestran al vendedor para responder).

#### Edge cases / errores

- Dos compradores pujan casi al mismo tiempo:
  - El sistema debe resolver por orden de llegada en backend.
  - El comprador que pierde esa carrera debe ver mensaje de “Tu puja fue superada por otro usuario”.
- Comprador con saldo insuficiente (si en futuro se integra pago in-app → TODO).
- Error de red al enviar puja (debe reintentar o mostrar error).

---

### 5.3 Subasta cerrada – comportamiento del comprador

#### Flujo si el comprador tiene la puja más alta

1. La subasta termina y el comprador resulta con la **puja ganadora**.
2. El sistema le solicita **confirmar su interés de compra**:
   - Puede **aceptar** o **rechazar**.
3. Si **acepta**:
   - Avanza al chat directo con el vendedor para acordar entrega y pago.
4. Si **rechaza**:
   - El sistema le pide **confirmar declinación** para evitar toques accidentales.
   - Una vez confirmada la declinación:
     - Se aplica una **penalización de 24 horas** en las que no puede participar en ninguna otra subasta.
     - El sistema pasa a la siguiente puja más alta (ver sección vendedor).
5. Una vez realizada la entrega:
   - El comprador confirma que recibió el producto.
   - Califica al vendedor.

#### Edge cases / errores

- El comprador no responde a la solicitud de confirmación dentro de un tiempo límite (ej. 24 horas):
  - Se considera “rechazo implícito”.
  - Se aplica penalización y se pasa al siguiente comprador → TODO definir plazos.
- El comprador afirma no haber recibido el producto aunque el vendedor marque como entregado:
  - Necesario sistema de resolución de disputas → TODO.
- El comprador intenta participar en otra subasta con penalización activa:
  - Bloqueo y mensaje claro sobre tiempo restante de penalización.

---

### 5.4 Historial de subastas (comprador)

- Lista de subastas en las que el usuario participó:
  - Como ganador.
  - Solo como participante (sin ganar).
  - Rechazó compra tras ganar (marcadas con indicador de penalización).
- Detalles:
  - Artículo.
  - Importe de puja ganadora (si aplica).
  - Vendedor.
  - Calificación que dio y que recibió.

---

## 6. Reglas transversales (básicas)

1. **Penalizaciones**
   - Duración estándar: 24 horas sin poder participar en ninguna subasta.
   - Causas iniciales:
     - Rechazar la compra tras tener la puja ganadora.
   - Futuras causas (reporte de fraude, no presentarse en la entrega, etc.) → TODO.

2. **Calificaciones**
   - Vendedor califica a comprador tras la entrega.
   - Comprador califica a vendedor tras la entrega.
   - Definir escala (ej. 1–5 estrellas) y criterios (cumplimiento, puntualidad, estado del producto, etc.) → TODO.

3. **Privacidad**
   - No compartir datos personales sensibles en las pantallas “públicas” de una subasta.
   - Compartir datos de contacto solo dentro de chats y acorde a la política de privacidad → TODO.

4. **Notificaciones**
   - Invitaciones a subastas.
   - Inicio de subasta.
   - Puja superada.
   - Fin de subasta.
   - Solicitudes de confirmación de compra.
   - Estado de penalización.
   - (Detalle de canales y frecuencia → TODO).

---

## 7. Pendientes / TODO (alto nivel)

- Definir stack tecnológico (frontend móvil, backend, base de datos, autenticación, etc.).
- Definir duración exacta de subastas y plazos de respuesta.
- Definir política de reactivación de subastas.
- Definir límites de invitados y reglas de revocación.
- Definir sistema de reportes y moderación.
- Definir mecánica de calificación y su impacto en confianza dentro de la app.
- Definir si en futuras versiones habrá manejo de pagos dentro de la app.
