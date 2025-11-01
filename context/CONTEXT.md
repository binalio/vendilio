# Vendilio - Documento de Contexto del Proyecto

## Resumen Ejecutivo

**Vendilio** es una plataforma móvil para subastas de artículos de segunda mano y cupones/promociones de negocios locales (PyMES), con enfoque en transacciones seguras entre conocidos y comunidades locales a nivel municipal.

**Nombre del proyecto:** Vendilio  
**Tagline:** "Vende fácil, compra mejor"

**Versión del documento:** 1.0  
**Fecha:** Octubre 2025  
**Estado:** Concepto inicial para MVP  
**Modelo de Desarrollo:** Solo founder con asistencia de IA

---

## Tabla de Contenidos

### 🚀 ESENCIAL PARA EMPEZAR
- **[0. Estrategia de Desarrollo en Solitario con IA](#0-estrategia-de-desarrollo-en-solitario-con-ia)** ⭐
  - Herramientas de IA recomendadas
  - Validación pre-código
  - Stack simplificado
  - Roadmap realista para 1 persona
  - Cómo trabajar efectivamente con IA
  - Presupuesto $300-1,000 USD
- **[21. Plan de Acción Paso a Paso](#21-plan-de-acción-paso-a-paso-solo-developer)** ⭐
  - Semana por semana
  - Prompts específicos
  - Checklist diario

### 📋 CONTEXTO DEL PRODUCTO
- [1. Problema que Resuelve](#1-problema-que-resuelve)
- [2. Propuesta de Valor](#2-propuesta-de-valor)
- [3. Tipos de Usuario](#3-tipos-de-usuario)
- [4. Funcionalidades Core (MVP)](#4-funcionalidades-core-mvp)
- [5. Flujos de Usuario Detallados](#5-flujos-de-usuario-detallados)

### 💻 ARQUITECTURA TÉCNICA
- [6. Arquitectura Técnica](#6-arquitectura-técnica)
  - Stack tecnológico
  - Base de datos
  - Endpoints API
- [7. Seguridad y Prevención de Fraude](#7-seguridad-y-prevención-de-fraude)

### 💰 NEGOCIO Y ESTRATEGIA
- [8. Modelo de Negocio](#8-modelo-de-negocio)
- [9. Roadmap de Desarrollo](#9-roadmap-de-desarrollo)
- [10. Métricas de Éxito](#10-métricas-de-éxito)
- [11. Riesgos y Mitigaciones](#11-riesgos-y-mitigaciones)
- [12. Competencia y Diferenciación](#12-competencia-y-diferenciación)

### ⚖️ LEGAL Y OPERACIONES
- [13. Consideraciones Legales](#13-consideraciones-legales)
- [14. Plan de Marketing (MVP)](#14-plan-de-marketing-mvp)

### 👥 RECURSOS
- [15. Equipo y Recursos (Desarrollo en Solitario)](#15-equipo-y-recursos-desarrollo-en-solitario) ⭐
- [16. Presupuesto Estimado (Solo Developer)](#16-presupuesto-estimado-solo-developer) ⭐
- [17. KPIs y Objetivos por Fase](#17-kpis-y-objetivos-por-fase)

### 📚 APÉNDICES
- [18. Preguntas Frecuentes](#18-preguntas-frecuentes-para-ai-assistants)
- [19. Próximos Pasos Recomendados](#19-próximos-pasos-recomendados)
- [20. Contacto y Mantenimiento](#20-contacto-y-mantenimiento-del-documento)
- [Apéndice A: Decisiones Clave del Diseño](#apéndice-a-decisiones-clave-del-diseño)
- [Apéndice B: Glosario de Términos](#apéndice-b-glosario-de-términos)
- [Apéndice C: Referencias y Recursos](#apéndice-c-referencias-y-recursos)

⭐ = Secciones críticas para desarrollo en solitario

---

## 0. Estrategia de Desarrollo en Solitario con IA

### 0.1 Realidad del Contexto

**Equipo:** 1 persona (tú) + Herramientas de IA  
**Implicaciones:**
- Tiempos de desarrollo más largos (6-9 meses vs 3 meses con equipo)
- Priorización MUY agresiva del MVP
- Usar herramientas que maximicen productividad
- Validar idea ANTES de invertir meses
- Automatizar todo lo posible
- Delegar a IA tareas repetitivas

### 0.2 Herramientas de IA Recomendadas

#### Para Desarrollo de Código
```
1. Claude (Anthropic) - Este documento
   - Arquitectura de sistema
   - Código completo de componentes
   - Debugging y optimización
   - Revisión de código
   - Documentación técnica

2. GitHub Copilot
   - Autocompletado inteligente
   - Generación de funciones
   - Sugerencias en tiempo real
   - $10/mes - VALE LA PENA

3. Cursor IDE
   - Editor con IA integrada
   - Chat con tu codebase
   - Multi-file editing
   - Refactoring inteligente

4. v0.dev (Vercel)
   - Generar componentes React/React Native
   - UI a partir de descripción
   - Gratis con límites
```

#### Para Diseño UI/UX
```
1. Figma + FigJam AI
   - Wireframes rápidos
   - Prototipos interactivos
   - Auto Layout con IA

2. Uizard
   - Texto → UI
   - Screenshot → código
   - $12-19/mes

3. Galileo AI
   - Describir pantalla → diseño completo
   - Genera UI editable

4. MidJourney / DALL-E
   - Iconos personalizados
   - Ilustraciones
   - Assets visuales
```

#### Para Testing y QA
```
1. Claude / ChatGPT
   - Generar casos de prueba
   - Scripts de testing
   - Identificar edge cases

2. Playwright (automatización)
   - Tests E2E automatizados
   - IA puede escribir los tests
```

#### Para Marketing y Contenido
```
1. Claude / ChatGPT
   - Copy para landing page
   - Posts de redes sociales
   - FAQs
   - Emails marketing

2. Canva AI
   - Diseño de materiales
   - Posts automáticos
   - Branding básico
```

### 0.3 Estrategia de Validación Pre-Código

**CRÍTICO: No escribas código hasta validar**

#### Semana 1-2: Validación Manual
```
Objetivo: Confirmar que alguien quiere esto

1. Crear formulario Google Forms:
   - "¿Usarías una app para subastar cosas entre conocidos?"
   - "¿Qué venderías/comprarías?"
   - "¿Usarías cupones de negocios locales?"

2. Encuestar a 50+ personas:
   - Amigos, familiares
   - Grupos de Facebook locales
   - WhatsApp groups

3. Hablar con 10 PyMES:
   - ¿Interés en subastar cupones?
   - ¿Cuánto pagarían?
   - ¿Qué necesitarían?

4. Criterio de éxito:
   - >60% dice "sí, lo usaría"
   - >30% da email para early access
   - >5 PyMES interesadas

Si NO pasas esto → Pivotear o abandonar
Si SÍ pasas → Continuar
```

#### Semana 3-4: MVP Sin Código (No-Code Prototype)
```
Objetivo: Simular la experiencia sin programar

Opción A: WhatsApp + Google Forms
1. Grupo de WhatsApp "Beta Testers"
2. Usuarios llenan form para "publicar subasta"
3. Tú manualmente publicas en grupo
4. Usuarios ofertan en WhatsApp
5. Coordinas entrega
6. Aprendes flujo real

Opción B: Notion + Airtable
1. Notion como "app"
2. Airtable como base de datos
3. Simulación del flujo completo
4. Sin escribir código

Si funciona y gente lo usa → Invertir en desarrollo
Si no → Evitaste meses de trabajo
```

### 0.4 Stack Simplificado para Solo Developer

#### Opción 1: Low-Code (Más Rápido) ⚡
```
Frontend: FlutterFlow o Bubble.io
Backend: Supabase (Firebase pero open source)
Auth: Supabase Auth
Base de Datos: Supabase (PostgreSQL)
Storage: Supabase Storage
Notificaciones: OneSignal

Ventajas:
✅ MVP en 4-6 semanas
✅ UI drag-and-drop
✅ Muchas integraciones
✅ Menos código = menos bugs

Desventajas:
❌ Menos control
❌ Puede ser limitado después
❌ Costos crecen con usuarios
```

#### Opción 2: React Native + Firebase (Más Control)
```
Frontend: React Native + Expo
Backend: Firebase
UI Kit: React Native Paper o NativeBase
Estado: Zustand (más simple que Redux)
Navegación: React Navigation
Forms: React Hook Form

Ventajas:
✅ Control total
✅ Escalable
✅ Comunidad grande
✅ Puede customizar todo

Desventajas:
❌ Más tiempo (3-4 meses)
❌ Más para aprender
❌ Más debugging
```

#### Opción 3: Híbrido (Recomendado) 🏆
```
FASE 1: Usar FlutterFlow para MVP rapidísimo
- Validar en 1 mes
- Conseguir primeros usuarios
- Aprender qué funciona

FASE 2: Si funciona, migrar a React Native
- Ahora sabes qué construir
- Invertir tiempo solo si validado
- Mejor producto final
```

### 0.5 Roadmap Realista para 1 Persona

#### Pre-Desarrollo (Mes 1)
```
Semana 1-2: Validación con encuestas
Semana 3-4: Prototipo no-code
Tiempo: 20-30 horas
Costo: $0
```

#### MVP Ultra Simplificado (Mes 2-4)
```
SOLO estas features:
✅ Login con teléfono (OTP)
✅ Publicar producto con foto
✅ Ver feed local de productos
✅ Hacer oferta simple
✅ Chat básico (Firebase Chat)
✅ Perfil mínimo

NO incluir todavía:
❌ Cupones de PyMES (fase 2)
❌ Subastas privadas
❌ Calificaciones complejas
❌ Notificaciones push
❌ Videos
❌ Múltiples fotos (solo 1)

Tiempo: 80-120 horas (20-30 hrs/semana)
Costo: $50/mes (Supabase/Firebase)
```

#### Testing con Usuarios (Mes 5)
```
Semana 1-2: Beta cerrada (10 usuarios)
Semana 3-4: Beta abierta (50 usuarios)
Semana 5-6: Iterar basado en feedback
Semana 7-8: Lanzamiento suave público

Tiempo: 40-60 horas fixes y ajustes
```

#### Iteración 2 (Mes 6-8)
```
Agregar features validadas:
✅ Subastas privadas
✅ Múltiples fotos
✅ Calificaciones
✅ Push notifications
✅ Piloto cupones (5 PyMES manuales)

Tiempo: 60-80 horas
```

**TOTAL: 6-8 meses de MVP a lanzamiento**

### 0.6 Cómo Trabajar con IA Efectivamente

#### Principios para Delegar a IA

**1. Contexto es Rey**
```
❌ MAL: "Crea una función de login"

✅ BIEN: "Crea una función de login en React Native que:
- Use Firebase Authentication
- Autentique con teléfono (OTP)
- Maneje estados de loading y error
- Navegue a HomeScreen si éxito
- Muestre error Toast si falla
- Incluya validación de formato de teléfono MX
- Use react-hook-form"
```

**2. Iteración Incremental**
```
Paso 1: Pide estructura básica
Paso 2: Pide manejo de errores
Paso 3: Pide validaciones
Paso 4: Pide tests
Paso 5: Pide optimizaciones

NO pidas todo junto o será genérico
```

**3. Usa Este Documento**
```
Cuando pidas código, incluye:
"Basado en el contexto del documento 
contexto-app-subastas.md, genera..."

La IA ya conoce tu arquitectura, 
decisiones y requisitos.
```

**4. Aprende de la IA**
```
No copies ciegamente
Lee el código generado
Pregunta: "¿Por qué usaste X en lugar de Y?"
Pide explicación de partes complejas
Construye conocimiento gradualmente
```

#### Prompt Templates Útiles

**Para Componentes UI:**
```
"Crea un componente React Native llamado [Nombre] que:
- Propósito: [descripción]
- Props: [listar props]
- Estado interno: [si aplica]
- Comportamiento: [qué hace]
- Estilo: [descripción visual]
- Manejo de errores: [casos edge]
- Accesibilidad: [consideraciones]

Usa TypeScript, React Native Paper para UI, 
y sigue mejores prácticas de React Hooks."
```

**Para Funciones Backend:**
```
"Crea una Cloud Function en Firebase que:
- Endpoint: POST /api/[ruta]
- Input: [describir payload]
- Validaciones: [qué validar]
- Lógica: [paso por paso]
- Output: [qué retorna]
- Errores: [casos a manejar]
- Seguridad: [reglas de auth]

Incluye comentarios explicando cada sección."
```

**Para Debugging:**
```
"Tengo este error: [copiar error completo]

Contexto:
- Estoy tratando de: [qué haces]
- Código relevante: [pegar código]
- Ya intenté: [qué probaste]

¿Cuál es el problema y cómo lo soluciono?"
```

**Para Arquitectura:**
```
"Necesito diseñar [feature X]

Requisitos:
1. [req 1]
2. [req 2]
...

Propón:
- Estructura de componentes
- Flujo de datos
- Qué librerías usar
- Posibles problemas
- Mejores prácticas

Dame opciones si hay varios enfoques."
```

### 0.7 Cronograma Semanal Realista

#### Si tienes trabajo de tiempo completo:

**20 horas/semana = MVP en 6-8 meses**

```
Lunes a Viernes: 2 horas/noche = 10 hrs
Sábado: 6 horas
Domingo: 4 horas
Total: 20 hrs/semana

Distribución:
- 40% Desarrollo (8 hrs)
- 30% Debugging/Testing (6 hrs)
- 20% Diseño/UI (4 hrs)
- 10% Aprendizaje/Docs (2 hrs)
```

#### Si puedes dedicar tiempo completo:

**40 horas/semana = MVP en 3-4 meses**

```
Lunes a Viernes: 8 horas/día = 40 hrs

Distribución:
- 50% Desarrollo (20 hrs)
- 20% Debugging/Testing (8 hrs)
- 15% Diseño/UI (6 hrs)
- 10% Marketing/Validación (4 hrs)
- 5% Aprendizaje/Docs (2 hrs)
```

### 0.8 Presupuesto Solo Developer

#### Inversión Mínima (Low-Code)
```
Mes 1 (Validación):
- $0 (solo tiempo)

Mes 2-4 (Desarrollo):
- FlutterFlow: $30/mes x 3 = $90
- Supabase: $25/mes x 3 = $75
- Dominio: $12/año = $12
- GitHub Copilot: $10/mes x 3 = $30
- Apple Developer: $99/año = $99
- Google Play: $25 único = $25

TOTAL: $331 USD (~ $6,000 MXN)
```

#### Inversión Estándar (React Native)
```
Mes 1 (Validación):
- $0

Mes 2-5 (Desarrollo):
- Firebase: $50/mes x 4 = $200
- Dominio: $12
- GitHub Copilot: $10/mes x 4 = $40
- Figma Pro: $15/mes x 4 = $60
- Apple Developer: $99
- Google Play: $25
- Curso Udemy (opcional): $15

TOTAL: $451 USD (~ $8,100 MXN)
```

**Conclusión: Puedes lanzar MVP con $300-500 USD**

### 0.9 Recursos de Aprendizaje

#### Si no sabes React Native:
```
1. Expo Docs (GRATIS): https://docs.expo.dev/
   - Tutorial oficial
   - 2-3 semanas part-time

2. YouTube: "React Native Tutorial 2024"
   - William Candillon
   - Traversy Media
   - GRATIS

3. Udemy ($15 en oferta):
   - "React Native - The Practical Guide"
   - Stephen Grider courses
```

#### Si no sabes Firebase:
```
1. Firebase Docs: https://firebase.google.com/docs
   - Codelabs interactivos
   - GRATIS

2. YouTube: "Firebase Full Course"
   - Fireship.io (excelente)
   - Net Ninja
   - GRATIS
```

**TIP:** No necesitas ser experto. Con IA, puedes aprender haciendo.

### 0.10 Señales de Alerta (Cuándo Parar)

```
🚩 SEÑALES ROJAS:
- Llevas 2 meses y no hay progreso visible
- Nadie respondió positivo en validación
- Te cuesta >80 horas entender lo básico
- Budget se acabó y no hay tracción
- Ya existen 3+ apps idénticas y exitosas
- PyMES no muestran interés real
- No disfrutas el proceso

✅ SEÑALES VERDES:
- Cada semana hay progreso tangible
- 10+ personas pidieron early access
- 5+ PyMES comprometidas para lanzamiento
- Aprendes y resuelves problemas
- Te emociona la visión
- Feedback positivo de pruebas
- Pequeñas victorias constantes
```

**Regla: Si a los 3 meses no hay tracción ni aprendizaje, reevaluar**

---

## 1. Problema que Resuelve

### 1.1 Para Vendedores Individuales
- Dificultad para vender artículos usados rápidamente
- Falta de confianza en plataformas de venta entre desconocidos
- Complejidad logística de envíos
- Desconfianza en métodos de pago online

### 1.2 Para PyMES
- Baja ocupación en horarios/días específicos
- Alto costo de publicidad digital
- Dificultad para atraer nuevos clientes
- Inventario o servicios sin vender

### 1.3 Para Compradores
- Desconfianza en vendedores desconocidos
- Riesgo de fraude en plataformas existentes
- Precios no competitivos
- Falta de ofertas locales relevantes

---

## 2. Propuesta de Valor

### 2.1 Diferenciadores Clave

**"Subastas privadas entre conocidos con entrega local"**

1. **Círculos de Confianza:** Posibilidad de subastar solo entre familiares, amigos o conocidos
2. **100% Local:** Enfoque municipal/estatal para eliminar complejidad de envíos
3. **Dual Market:** Productos de segunda mano + cupones/promociones de negocios
4. **Subastas Express:** Velocidad para vender rápido
5. **Seguridad por Diseño:** QR dinámicos, calificaciones, zonas seguras sugeridas

### 2.2 Ventaja Competitiva vs Competencia

| Competidor | Lo que NO tienen |
|------------|------------------|
| Mercado Libre | Subastas privadas, enfoque 100% local |
| Wallapop | Formato subasta, cupones de negocios |
| Facebook Marketplace | Estructura formal, subastas temporales |
| Groupon | Formato subasta, enfoque local granular |
| eBay | Círculos privados, cupones de PyMES locales |

---

## 3. Tipos de Usuario

### 3.1 Vendedores Individuales
- **Perfil:** Personas con artículos usados en casa/negocio
- **Motivación:** Liberar espacio, recuperar algo de inversión, ayudar a conocidos
- **Casos de uso:** Electrónicos usados, muebles, ropa, juguetes, libros, artículos de hogar

### 3.2 PyMES (Negocios Locales)
- **Perfil:** Restaurantes, cafeterías, gimnasios, salones de belleza, spas, cines locales
- **Motivación:** Llenar horarios muertos, atraer clientes nuevos, generar flujo de caja
- **Casos de uso:** Cupones de descuento, promociones flash, paquetes de servicios

### 3.3 Compradores/Postores
- **Perfil:** Personas buscando ahorrar, cazadores de ofertas, coleccionistas
- **Motivación:** Ahorrar dinero, encontrar artículos únicos, apoyar negocios locales
- **Comportamiento:** Participan en subastas, hacen ofertas, comparan precios

### 3.4 Observadores
- **Perfil:** Usuarios explorando la plataforma
- **Motivación:** Curiosidad, investigación de mercado, aprender sobre precios
- **Comportamiento:** Navegan sin participar activamente

---

## 4. Funcionalidades Core (MVP)

### 4.1 Para Vendedores Individuales

#### Registro y Verificación
- Crear cuenta con teléfono (verificación SMS)
- Aceptar términos y condiciones
- Ubicar estado y municipio

#### Crear Anuncio de Producto
- Tomar fotos o videos cortos del artículo
- Descripción del producto
- Configurar:
  - Precio mínimo de subasta
  - Duración de la subasta (opciones: 6h, 12h, 24h, 48h)
  - Forma de pago: **Efectivo contra entrega (único método en MVP)**
- Definir zona segura de entrega (lugares públicos sugeridos)

#### Opciones de Visibilidad
- **Privada:** Invitar solo a contactos específicos (WhatsApp/link compartible)
- **Pública:** Visible para todos los usuarios del mismo municipio

#### Durante la Subasta
- Chat simple de preguntas y respuestas con interesados
- Ver ofertas en tiempo real
- Notificaciones push de nuevas ofertas

#### Post-Subasta
- Si hay ganador: Abrir chat 1-a-1 para coordinar entrega
- Si no hay ofertas: Opción de republicar al día siguiente
- Calificar al comprador después de la entrega (⭐ 1-5)

### 4.2 Para PyMES

#### Verificación
- Registro con validación manual inicial
- Subir documentación (RFC, identificación)
- Verificación de existencia del negocio

#### Crear Promoción/Cupón
- Título de la promoción
- Descripción detallada (qué incluye/excluye)
- Precio regular vs precio de subasta inicial
- Cantidad de cupones disponibles (tiraje limitado)
- Vigencia (días de validez desde la compra)
- Restricciones (horarios, días, condiciones)
- Fotos del producto/servicio

#### Gestión de Cupones
- Dashboard de cupones vendidos
- Scanner QR para validar cupones
- Ver estadísticas básicas (vendidos, redimidos, pendientes)

### 4.3 Para Compradores

#### Explorar y Ofertar
- Ver subastas activas en su municipio
- Filtrar por categoría, precio, distancia
- Hacer ofertas en subastas públicas
- Participar en subastas privadas (si fueron invitados)
- Recibir notificaciones si son superados

#### Gestionar Cupones Ganados
- Ver "Mis Cupones" activos
- Botón "Usar Ahora" que genera QR dinámico (válido 2-3 minutos)
- Ver detalles de la promoción
- Recibir notificaciones antes de expirar

#### Post-Compra
- Chat con vendedor para coordinar entrega
- Calificar al vendedor (⭐ 1-5)
- Historial de compras

---

## 5. Flujos de Usuario Detallados

### 5.1 Flujo: Vender Artículo de Segunda Mano

```
1. Usuario crea cuenta → Verifica teléfono
2. Acepta términos y condiciones
3. Selecciona ubicación (estado, municipio)
4. Toca "Crear Anuncio" → Selecciona "Producto"
5. Toma fotos/videos del artículo
6. Escribe descripción
7. Configura:
   - Precio mínimo: $100
   - Duración: 24 horas
   - Pago: Efectivo
   - Zona de entrega: Plaza comercial central
8. Elige visibilidad: Público (todo su municipio)
9. Publica anuncio
10. Recibe notificaciones de ofertas
11. Al terminar tiempo: Ve ganador
12. Abre chat con ganador
13. Coordina día, hora, lugar de entrega
14. Se reúnen en zona segura
15. Entrega artículo, recibe efectivo
16. Ambos se califican mutuamente
```

### 5.2 Flujo: PyME Crea Cupón Promocional

```
1. PyME se registra → Verificación manual (admin revisa)
2. Aprobación (1-2 días)
3. Toca "Crear Promoción"
4. Completa información:
   - Título: "Pizza Familiar 40% descuento"
   - Precio regular: $250
   - Precio inicial subasta: $100
   - Cantidad: 20 cupones
   - Vigencia: 30 días desde compra
   - Restricciones: "Solo cenas, no acumulable"
5. Sube foto de la pizza
6. Publica promoción
7. Usuarios subastan
8. Al terminar: Top 20 ofertas ganan
9. Cada ganador recibe cupón digital
10. Cuando cliente llega al negocio:
    - Cliente genera QR dinámico desde app
    - PyME escanea QR
    - Sistema valida y marca como usado
    - PyME entrega el producto/servicio
```

### 5.3 Flujo: Comprador Participa en Subasta

```
1. Usuario navega feed de subastas activas
2. Ve artículo interesante: iPhone 12, precio min $2,000
3. Toca para ver detalles
4. Lee descripción, ve fotos
5. Hace oferta inicial: $2,500
6. Recibe notificación: "Alguien ofertó $2,600"
7. Aumenta oferta a $2,800
8. Termina subasta → Gana
9. Recibe notificación: "¡Ganaste!"
10. Abre chat con vendedor
11. Acuerdan: "Mañana 5pm en Starbucks de Av. Central"
12. Al día siguiente se reúnen
13. Comprador revisa artículo
14. Paga $2,800 en efectivo
15. Ambos califican: 5 estrellas
```

### 5.4 Flujo: Usar Cupón con QR Dinámico

```
1. Usuario ganó cupón de Pizza Familiar
2. Decide ir hoy al restaurante
3. Abre app → "Mis Cupones"
4. Ve cupón: "Pizza Familiar - Válido hasta: 30 Nov"
5. Llega al restaurante
6. Toca "USAR AHORA"
7. (Opcional) Verifica con Face ID/Huella
8. App genera QR dinámico (válido 3 minutos)
9. Muestra pantalla con:
   - QR code grande
   - Countdown: "Expira en 02:45"
   - Detalles de la promo
10. Empleado escanea QR con app del negocio
11. Backend valida:
    - ✅ Token válido
    - ✅ No expirado
    - ✅ Negocio correcto
    - ✅ Cupón activo
12. Marca cupón como "usado"
13. Elimina token temporal
14. Ambas apps muestran: "✅ Cupón validado"
15. Restaurante prepara y entrega pizza
16. Usuario califica experiencia
```

---

## 6. Arquitectura Técnica

### 6.1 Stack Tecnológico Recomendado

```
Frontend Mobile:
- React Native (iOS + Android desde una base de código)
- Expo (opcional para desarrollo rápido MVP)
- React Navigation (navegación)
- React Native Camera (scanner QR)
- react-native-qrcode-svg (generar QR)

Backend:
- Node.js + Express (API REST)
- Firebase o Supabase (alternativa open source)
  * Authentication (Auth)
  * Firestore (Base de datos NoSQL)
  * Cloud Storage (Imágenes/videos)
  * Cloud Functions (lógica serverless)
  * Cloud Messaging (Push notifications)

Cache/Tokens Temporales:
- Redis (para tokens QR temporales)
- O Firestore con TTL automático

Pagos (Fase 2):
- Stripe Connect o MercadoPago

Hosting:
- Firebase Hosting o Vercel
- App móvil: Apple App Store + Google Play Store

Estimado de costos iniciales: $50-100/mes
```

### 6.2 Estructura de Base de Datos

#### Colección: `usuarios`
```javascript
{
  id: "user_123",
  nombre: "Juan Pérez",
  telefono: "+52XXXXXXXXXX",
  telefono_verificado: true,
  email: "juan@email.com",
  ubicacion: {
    estado: "Querétaro",
    municipio: "Santiago de Querétaro"
  },
  tipo: "individual" | "pyme",
  calificacion_promedio: 4.8,
  total_ventas: 15,
  total_compras: 23,
  creado_at: "2025-10-15T10:30:00Z",
  activo: true
}
```

#### Colección: `anuncios_productos`
```javascript
{
  id: "prod_456",
  vendedor_id: "user_123",
  titulo: "iPhone 12 Pro 128GB",
  descripcion: "Excelente estado, batería 95%...",
  categoria: "electrónica",
  imagenes: ["url1", "url2", "url3"],
  videos: ["url_video"],
  precio_minimo: 5000,
  precio_actual: 6500,
  estado_articulo: "usado_bueno",
  duracion_horas: 24,
  fecha_inicio: "2025-10-31T08:00:00Z",
  fecha_fin: "2025-11-01T08:00:00Z",
  visibilidad: "publica" | "privada",
  invitados: ["user_789", "user_012"], // si es privada
  ubicacion: {
    estado: "Querétaro",
    municipio: "Santiago de Querétaro",
    zona_entrega: "Plaza Antea"
  },
  forma_pago: ["efectivo"],
  estado_subasta: "activa" | "finalizada" | "cancelada",
  ganador_id: null,
  total_ofertas: 12,
  creado_at: "2025-10-31T08:00:00Z"
}
```

#### Colección: `ofertas`
```javascript
{
  id: "oferta_789",
  anuncio_id: "prod_456",
  usuario_id: "user_321",
  monto: 6500,
  fecha: "2025-10-31T14:30:00Z",
  estado: "activa" | "superada" | "ganadora"
}
```

#### Colección: `promociones`
```javascript
{
  id: "promo_101",
  negocio_id: "pyme_202",
  titulo: "Pizza Familiar 40% OFF",
  descripcion: "Pizza grande de hasta 3 ingredientes...",
  imagen: "url",
  precio_regular: 250,
  precio_inicial_subasta: 100,
  cantidad_cupones: 20,
  cupones_vendidos: 18,
  vigencia_dias: 30,
  restricciones: "Solo cenas, no acumulable con otras promos",
  categoria: "alimentos",
  fecha_inicio: "2025-11-01T00:00:00Z",
  fecha_fin: "2025-11-01T23:59:59Z",
  estado: "activa" | "finalizada" | "cancelada"
}
```

#### Colección: `cupones`
```javascript
{
  id: "cupon_303",
  promo_id: "promo_101",
  usuario_id: "user_321",
  negocio_id: "pyme_202",
  precio_pagado: 150,
  fecha_compra: "2025-11-01T20:00:00Z",
  fecha_expiracion: "2025-12-01T23:59:59Z",
  estado: "activo" | "usado" | "expirado",
  fecha_uso: null,
  codigo_referencia: "CUP-2025-303"
}
```

#### Colección: `qr_tokens` (Redis o Firestore con TTL)
```javascript
{
  token: "a1b2c3d4e5f6...",
  cupon_id: "cupon_303",
  usuario_id: "user_321",
  negocio_id: "pyme_202",
  created_at: "2025-11-05T18:30:00Z",
  expires_at: "2025-11-05T18:33:00Z", // 3 minutos
  used: false
}
```

#### Colección: `calificaciones`
```javascript
{
  id: "rating_404",
  de_usuario_id: "user_321",
  para_usuario_id: "user_123",
  anuncio_id: "prod_456",
  tipo: "vendedor" | "comprador",
  estrellas: 5,
  comentario: "Excelente vendedor, todo como lo describió",
  fecha: "2025-11-02T10:00:00Z"
}
```

#### Colección: `chats`
```javascript
{
  id: "chat_505",
  anuncio_id: "prod_456",
  participantes: ["user_123", "user_321"],
  tipo: "producto" | "cupon",
  ultimo_mensaje: "Nos vemos mañana a las 5pm",
  fecha_ultimo_mensaje: "2025-11-01T16:00:00Z",
  creado_at: "2025-10-31T15:00:00Z"
}
```

#### Colección: `mensajes`
```javascript
{
  id: "msg_606",
  chat_id: "chat_505",
  de_usuario_id: "user_321",
  texto: "¿El iPhone incluye cargador?",
  fecha: "2025-10-31T15:05:00Z",
  leido: true
}
```

### 6.3 Endpoints API Principales

#### Autenticación
```
POST /api/auth/register
POST /api/auth/verify-phone
POST /api/auth/login
POST /api/auth/logout
```

#### Productos (Segunda Mano)
```
POST /api/productos/crear
GET /api/productos/listar?municipio=xxx&categoria=xxx
GET /api/productos/:id
PUT /api/productos/:id/editar
DELETE /api/productos/:id
POST /api/productos/:id/ofertar
GET /api/productos/:id/ofertas
```

#### Promociones (PyMES)
```
POST /api/promociones/crear
GET /api/promociones/listar?municipio=xxx&categoria=xxx
GET /api/promociones/:id
POST /api/promociones/:id/ofertar
```

#### Cupones
```
GET /api/cupones/mis-cupones
POST /api/cupones/generar-qr
POST /api/cupones/validar-qr
GET /api/cupones/:id
```

#### Usuarios
```
GET /api/usuarios/perfil
PUT /api/usuarios/perfil
GET /api/usuarios/:id/calificaciones
POST /api/usuarios/:id/calificar
```

#### Chat
```
GET /api/chats/mis-chats
POST /api/chats/crear
GET /api/chats/:id/mensajes
POST /api/chats/:id/enviar
```

---

## 7. Seguridad y Prevención de Fraude

### 7.1 QR Dinámico para Cupones

**Arquitectura de Seguridad:**

```javascript
// Generación de QR temporal
1. Usuario toca "Usar Ahora" en cupón
2. App solicita token temporal al backend
3. Backend:
   - Valida usuario autenticado
   - Valida cupón existe y es activo
   - Genera token único aleatorio
   - Guarda en Redis con TTL de 180 segundos
   - Retorna token
4. App genera QR visual del token
5. Muestra QR con countdown (3 minutos)
6. Detecta screenshots → invalida token

// Validación por negocio
1. Negocio escanea QR
2. Lee token del QR
3. Envía a backend para validar
4. Backend verifica:
   - Token existe en Redis
   - No ha expirado
   - Negocio ID coincide
   - Cupón aún activo
5. Si OK: Marca cupón como usado + elimina token
6. Si NO: Rechaza con mensaje de error
7. Log de la transacción
```

**Medidas Anti-Fraude:**
- Token expira en 180 segundos
- Solo válido para negocio específico
- Detección de screenshots (opcional)
- Geolocalización (opcional en Fase 2)
- Verificación biométrica (opcional)
- Límite de generaciones de QR por cupón: 5
- Watermark personalizado en QR (nombre usuario + timestamp)

### 7.2 Sistema de Calificaciones

```
Objetivo: Generar confianza entre usuarios

Mecánica:
- Comprador y vendedor se califican mutuamente
- Escala 1-5 estrellas
- Comentario opcional
- Solo después de completar transacción
- No editable después de publicado
- Promedio visible en perfil

Aspectos a calificar:
Vendedores: Descripción precisa, puntualidad, estado del producto, amabilidad
Compradores: Puntualidad, pago correcto, trato respetuoso
```

### 7.3 Moderación de Contenido

**Artículos Prohibidos:**
- Armas, drogas, medicamentos
- Productos falsificados
- Contenido explícito
- Animales vivos
- Documentos oficiales

**Sistema de Reportes:**
- Botón "Reportar" en cada anuncio
- Motivos: Fraude, artículo prohibido, contenido inapropiado, spam
- Revisión manual (fase inicial)
- Automatización con IA (fase posterior)

### 7.4 Zonas Seguras de Entrega

**Sugerencias:**
- Plazas comerciales
- Cafeterías conocidas
- Estacionamientos públicos vigilados
- Dentro de tiendas departamentales
- Lobby de bancos (horario laboral)

**Disclaimer Legal:**
```
"La aplicación NO se hace responsable por la seguridad 
de las transacciones. Se recomienda fuertemente:
- Reunirse en lugares públicos
- Horarios diurnos con buena iluminación
- Llevar acompañante si es posible
- Avisar a familiares de la ubicación
- Revisar artículo antes de pagar"
```

---

## 8. Modelo de Negocio

### 8.1 MVP (Primeros 6 meses)

**Estrategia: GRATIS para todos**

Objetivo: Conseguir tracción, validar producto, crecer base de usuarios

Métricas de éxito:
- 1,000+ usuarios activos
- 500+ transacciones completadas
- Tasa de conversión subasta → venta > 30%
- Usuarios que regresan > 40%
- NPS (Net Promoter Score) > 50

### 8.2 Fase 2: Monetización (Mes 6+)

**Opción A: Comisión por Venta**
```
Productos de segunda mano: 5% comisión
Cupones de PyMES: 10-15% comisión

Ventajas:
- Solo pagas si vendes
- Justo para usuarios casuales
- Escalable

Ejemplo:
- Vendo artículo en $1,000
- Comisión: $50
- Recibo: $950
```

**Opción B: Freemium para PyMES**
```
PLAN GRATUITO:
- 3 promociones/mes
- Sin destacar
- Estadísticas básicas

PLAN PRO ($299-499/mes):
- Promociones ilimitadas
- Destacar automáticamente
- Badge "Verificado"
- Estadísticas avanzadas
- Soporte prioritario
```

**Opción C: Publicaciones Destacadas**
```
Vendedores pagan $1-3 para destacar anuncio
- Aparece arriba del feed 24-48 horas
- Badge "Destacado"
- Más visibilidad = más ofertas
```

**Opción D: Modelo Híbrido (Recomendado)**
```
- Base gratis para usuarios individuales (primeros 5 productos/mes)
- Después: 5% comisión o $2 por publicación
- PyMES: 10% comisión por cupón vendido O $299/mes ilimitado
- Destacados: $1-3 por artículo
```

### 8.3 Proyección de Ingresos (Año 1)

**Escenario Conservador:**
```
Mes 6 (inicio monetización):
- 2,000 usuarios activos
- 800 transacciones/mes
- Ticket promedio: $500
- Comisión 5% = $20,000 MXN/mes

Mes 12:
- 5,000 usuarios activos
- 2,000 transacciones/mes
- 50 PyMES con plan Pro ($299/mes)
- Ingresos productos: $50,000 MXN
- Ingresos PyMES: $15,000 MXN
- Total: $65,000 MXN/mes (~$3,900 USD)
```

---

## 9. Roadmap de Desarrollo

### Fase 1: MVP (Meses 1-3)

**Objetivo:** Validar concepto con funcionalidades core

**Alcance:**
- ✅ Registro y autenticación (SMS)
- ✅ Crear/publicar productos de segunda mano
- ✅ Subastas públicas y privadas (solo municipal)
- ✅ Sistema de ofertas
- ✅ Chat 1-a-1 básico
- ✅ Calificaciones simples (⭐)
- ✅ Perfil de usuario
- ✅ Notificaciones push básicas
- ✅ Solo efectivo como método de pago

**NO incluye:**
- ❌ Cupones de PyMES
- ❌ Pagos integrados
- ❌ IA para sugerencias
- ❌ Envíos coordinados
- ❌ Múltiples estados/municipios

**KPIs de éxito:**
- 500 usuarios registrados
- 100 transacciones completadas
- 30% tasa de conversión
- 70% usuarios satisfechos (encuesta)

### Fase 1.5: Piloto Cupones (Mes 4)

**Objetivo:** Validar modelo de cupones con control estricto

**Alcance:**
- ✅ Onboarding manual de 5-10 PyMES
- ✅ Crear/publicar promociones
- ✅ Sistema de cupones digitales
- ✅ QR dinámico para validación
- ✅ Scanner app para negocios
- ✅ Dashboard básico para PyMES

**Proceso:**
1. Seleccionar 5-10 PyMES de categorías seguras (restaurantes, cafés, gimnasios)
2. Verificar manualmente cada negocio
3. Entrenar en uso de la app
4. Publicar primera ola de promociones
5. Monitorear de cerca
6. Recolectar feedback intensivo

**KPIs de éxito:**
- 5+ PyMES activas
- 200+ cupones vendidos
- 80%+ redimidos
- 4+ estrellas promedio de usuarios

### Fase 2: Escalar (Meses 5-8)

**Objetivo:** Crecer usuarios y funcionalidades

**Alcance:**
- ✅ Abrir cupones a más PyMES (verificación semi-automática)
- ✅ Expandir a más municipios del estado
- ✅ Subastas express (30 min, 1 hora)
- ✅ Republicar automática con suscripción
- ✅ Filtros avanzados y búsqueda
- ✅ Sistema de favoritos
- ✅ Historial de transacciones
- ✅ Iniciar monetización (comisiones bajas)

**Marketing:**
- Campañas en redes sociales locales
- Alianzas con PyMES para promo cruzada
- Programa de referidos (invita y gana)

### Fase 3: Optimización (Meses 9-12)

**Objetivo:** Perfeccionar producto y aumentar retención

**Alcance:**
- ✅ Integración de pagos (Stripe/MercadoPago)
- ✅ Pasarela segura para garantizar transacciones
- ✅ Envíos coordinados (alianza con mensajería)
- ✅ IA para sugerir precios (basado en históricos)
- ✅ Sugerencias personalizadas
- ✅ Programa de lealtad/puntos
- ✅ App web (además de móvil)
- ✅ Expandir a múltiples estados

**Monetización activa:**
- Planes premium para PyMES
- Comisiones consolidadas
- Destacados pagados

### Fase 4: Escala Nacional (Año 2)

**Objetivo:** Convertirse en la plataforma líder nacional

**Alcance:**
- ✅ Cobertura nacional
- ✅ Categorías especializadas
- ✅ Verificación de identidad avanzada
- ✅ Seguros para transacciones de alto valor
- ✅ API para terceros
- ✅ Programa de afiliados
- ✅ Analytics avanzado para PyMES
- ✅ Soporte 24/7

---

## 10. Métricas de Éxito

### 10.1 Métricas de Producto

**Adquisición:**
- Descargas de la app
- Registros completados
- Tasa de conversión registro → primera acción

**Activación:**
- Usuarios que publican primer anuncio
- Usuarios que hacen primera oferta
- Tiempo promedio hasta primera transacción

**Engagement:**
- DAU (Usuarios Activos Diarios)
- MAU (Usuarios Activos Mensuales)
- Sesiones por usuario/semana
- Tiempo promedio en app

**Retención:**
- % usuarios que regresan al día 1, 7, 30
- Churn rate mensual
- Lifetime Value (LTV)

**Referral:**
- % usuarios que invitan a otros
- Viralidad (K-factor)

### 10.2 Métricas de Negocio

**Transacciones:**
- Subastas publicadas/día
- Tasa de conversión (subasta → venta)
- Ticket promedio
- GMV (Gross Merchandise Value) mensual

**Cupones:**
- Promociones publicadas
- Cupones vendidos
- Tasa de redención
- Ingresos por comisiones

**Calidad:**
- NPS (Net Promoter Score)
- Calificación promedio de usuarios
- % transacciones con incidentes
- Tiempo de respuesta de soporte

---

## 11. Riesgos y Mitigaciones

### 11.1 Riesgos Técnicos

| Riesgo | Probabilidad | Impacto | Mitigación |
|--------|--------------|---------|------------|
| Escalabilidad del sistema | Media | Alto | Usar Firebase/cloud nativo desde día 1 |
| Fraude en QR | Media | Alto | Sistema de tokens temporales + logs |
| Caída de servidores | Baja | Alto | Infraestructura cloud con auto-scaling |
| Bugs críticos | Alta | Medio | Testing exhaustivo + beta testers |

### 11.2 Riesgos de Negocio

| Riesgo | Probabilidad | Impacto | Mitigación |
|--------|--------------|---------|------------|
| Baja adopción inicial | Alta | Alto | Marketing local agresivo + referidos |
| PyMES no adoptan cupones | Media | Medio | Prueba de concepto con 5-10 primeros |
| Competencia copia modelo | Media | Medio | Velocidad de ejecución + comunidad fuerte |
| Fraudes entre usuarios | Media | Alto | Sistema de calificaciones + reportes |

### 11.3 Riesgos Legales

| Riesgo | Probabilidad | Impacto | Mitigación |
|--------|--------------|---------|------------|
| Responsabilidad por transacciones | Alta | Alto | Disclaimer claro + T&C robustos |
| Venta de artículos ilegales | Media | Alto | Moderación + lista de prohibidos |
| Protección de datos (GDPR/LFPDPPP) | Alta | Alto | Cumplimiento desde diseño |
| Disputas de pago | Media | Medio | Sistema de reportes + mediación |

---

## 12. Competencia y Diferenciación

### 12.1 Análisis Competitivo

| Plataforma | Fortaleza | Debilidad | Nuestra Ventaja |
|------------|-----------|-----------|-----------------|
| **Mercado Libre** | Alcance nacional, confianza | Complejo, envíos, comisiones altas | Subastas privadas, 100% local, simple |
| **Facebook Marketplace** | Base de usuarios gigante | Sin estructura, fraudes, spam | Formato profesional, subastas temporales |
| **Wallapop** | UI simple, chat integrado | Sin subastas, sin cupones | Formato subasta + cupones PyMES |
| **Groupon** | Modelo establecido de cupones | Sin subastas, nacional, precio fijo | Subasta de cupones, hiperlocal |
| **OfferUp** | Popular en USA | No en México, sin cupones | Mercado local + cupones locales |

### 12.2 Propuesta Única de Valor

**"La única app donde puedes subastar entre conocidos Y conseguir cupones de tus negocios favoritos locales"**

Elementos diferenciadores:
1. **Subastas privadas** (único)
2. **Dual market:** Productos + Servicios (cupones)
3. **Hiperlocal:** Municipal/estatal
4. **Sin envíos en MVP:** Menos fricción
5. **QR dinámico:** Seguridad única
6. **Express:** Vende en horas, no días

---

## 13. Consideraciones Legales

### 13.1 Términos y Condiciones Clave

**Responsabilidad:**
```
"La plataforma actúa únicamente como intermediario 
para conectar compradores y vendedores. No somos 
responsables de:
- La calidad, legalidad o autenticidad de los productos
- El comportamiento de los usuarios
- Transacciones fuera de la plataforma
- Seguridad física durante encuentros
- Productos dañados o defectuosos
"
```

**Obligaciones del Usuario:**
- Solo vender artículos que legalmente posee
- No vender artículos de la lista prohibida
- Describir honestamente los productos
- Respetar precios acordados en subasta
- Reportar comportamiento sospechoso

### 13.2 Política de Privacidad

**Datos recopilados:**
- Nombre, teléfono, ubicación (municipio)
- Historial de transacciones
- Mensajes en chat
- Calificaciones
- Fotos/videos subidos

**Uso de datos:**
- Proveer el servicio
- Mejorar experiencia
- Prevenir fraude
- Análisis agregado
- Marketing (con consentimiento)

**NO compartimos con terceros excepto:**
- Procesadores de pago
- Servicios en la nube (Firebase)
- Requerimiento legal

### 13.3 Lista de Artículos Prohibidos

```
❌ Armas, municiones, explosivos
❌ Drogas, sustancias controladas
❌ Medicamentos con receta
❌ Productos falsificados
❌ Contenido sexual explícito
❌ Animales vivos
❌ Documentos oficiales (IDs, pasaportes)
❌ Órganos humanos
❌ Productos robados
❌ Servicios ilegales
❌ Alcohol (sin licencia)
❌ Tabaco
```

---

## 14. Plan de Marketing (MVP)

### 14.1 Estrategia de Lanzamiento

**Pre-Lanzamiento (4 semanas antes):**
1. Landing page con registro de interés
2. Recolectar 200+ emails
3. Crear expectativa en redes sociales
4. Contactar influencers locales micro
5. Alianzas con 5-10 PyMES para lanzamiento

**Lanzamiento Suave (Semana 1-2):**
1. Invitar primeros 100 usuarios (de emails)
2. Monitoreo intenso de bugs
3. Recolectar feedback directo
4. Iterar rápido

**Lanzamiento Público (Semana 3-4):**
1. Abrir registros públicos
2. Campaña en redes sociales locales
3. Volantes en universidades
4. Promoción cruzada con PyMES aliadas

### 14.2 Canales de Adquisición

**Orgánico:**
- Redes sociales (Facebook, Instagram, TikTok)
- Boca a boca
- Programa de referidos
- SEO local

**Pagado (Budget inicial $500-1,000 USD/mes):**
- Facebook/Instagram Ads (geolocalizado)
- Google Ads (keywords locales)
- Colaboraciones con influencers locales

**Partnerships:**
- Cámaras de comercio locales
- Asociaciones de PyMES
- Universidades (estudiantes como early adopters)

### 14.3 Mensajes Clave

**Para vendedores individuales:**
"Vende lo que no usas entre conocidos de forma rápida y segura"

**Para PyMES:**
"Llena tus horarios muertos con subastas de cupones. Solo pagas si vendes"

**Para compradores:**
"Consigue las mejores ofertas locales y apoya a tu comunidad"

---

## 15. Equipo y Recursos (Desarrollo en Solitario)

### 15.1 Para MVP - Solo Developer + IA

**TÚ serás:**
- ✅ Product Manager (defines visión)
- ✅ Developer (con IA escribiendo ~60% del código)
- ✅ Designer (con herramientas de IA)
- ✅ QA Tester (tú + beta testers amigos)
- ✅ Marketing inicial (redes sociales básicas)

**Tu "equipo" de IA:**
- Claude / ChatGPT: Arquitectura, código, documentación
- GitHub Copilot: Autocompletado mientras codeas
- Figma + IA plugins: Diseño UI
- Canva AI: Marketing assets

**Outsourcing opcional (si budget permite):**
- Legal freelancer: T&C ($200-500 USD) - VALE LA PENA
- Beta testers: 10-20 amigos/conocidos - GRATIS
- Diseñador freelance (Fiverr): Iconos/logo ($50-100) - OPCIONAL

### 15.2 Post-MVP (Si validas y quieres crecer)

**Primeras contrataciones (en orden):**
1. **Customer Support part-time** (mes 6-8)
   - Responder usuarios
   - Moderar contenido
   - $500-800/mes

2. **Desarrollador Junior part-time** (mes 9-12)
   - Te ayuda con bugs
   - Features secundarias
   - $1,000-1,500/mes

3. **Community Manager freelance** (mes 6+)
   - Redes sociales
   - Contenido
   - $300-600/mes

**Contratar SOLO cuando:**
- ✅ Tienes revenue para pagar
- ✅ Más de 1,000 usuarios activos
- ✅ No puedes manejar todo
- ✅ Validaste product-market fit

### 15.3 Herramientas que Reemplazan Equipo

| Rol | Herramienta | Costo |
|-----|-------------|-------|
| Desarrollador | Claude + Copilot + Cursor | $10-30/mes |
| Diseñador | Figma + Galileo AI + v0.dev | $15-30/mes |
| QA | Amigos beta testers | Gratis |
| Marketing | Canva AI + ChatGPT | $0-15/mes |
| Analytics | Firebase Analytics | Gratis |
| Customer Support (inicial) | Tú mismo + ChatGPT templates | Gratis |
| Legal | Termly.io (genera T&C) | $15/mes |

**Total mensual: $40-90 USD** - 95% más barato que contratar humanos

---

## 16. Presupuesto Estimado (Solo Developer)

### 16.1 Desarrollo MVP (4-6 meses)

#### OPCIÓN A: Ruta Low-Code (Más Rápida)
```
Herramientas de Desarrollo:
- FlutterFlow: $30/mes x 4 = $120
- Supabase (backend): $25/mes x 4 = $100
- GitHub Copilot: $10/mes x 4 = $40
- Figma Free: $0
- Dominio .com: $12/año = $12

Publicación Apps:
- Apple Developer: $99/año = $99
- Google Play Developer: $25 único = $25

Legal/Administrativo:
- Termly (T&C generator): $15/mes x 2 = $30
- O freelancer legal: $200-300 (opcional)

Marketing Inicial:
- Canva Pro: $13/mes x 2 = $26
- Ads Facebook: $100 (para lanzamiento)

TOTAL OPCIÓN A: $522-822 USD
(~ $9,400 - 14,800 MXN)
```

#### OPCIÓN B: Ruta React Native (Más Control)
```
Herramientas de Desarrollo:
- Firebase (Blaze plan): $50/mes x 4 = $200
- GitHub Copilot: $10/mes x 4 = $40
- Cursor IDE: $20/mes x 4 = $80
- Figma Pro: $15/mes x 4 = $60
- Dominio: $12

Publicación Apps:
- Apple Developer: $99
- Google Play: $25

Legal:
- Termly: $15/mes x 2 = $30
- O freelancer: $200-300

Aprendizaje (opcional):
- Curso Udemy: $15
- Docs React Native: GRATIS

Marketing:
- Canva Pro: $13/mes x 2 = $26
- Ads: $100

TOTAL OPCIÓN B: $687-987 USD
(~ $12,400 - 17,800 MXN)
```

### 16.2 Operación Post-Lanzamiento (Meses 7-12)

```
Infraestructura:
- Firebase/Supabase: $50-100/mes
- Dominio: Incluido
- Apple/Google fee: Incluido año 1

Herramientas:
- Copilot: $10/mes
- Figma: $15/mes (si sigues Pro)
- Analytics: GRATIS (Firebase)

Marketing:
- Ads: $100-300/mes (según resultados)
- Contenido: $0 (tú + ChatGPT)

Contingencias:
- $50-100/mes

TOTAL MENSUAL: $225-525/mes
```

### 16.3 Comparación de Inversión

| Enfoque | Inversión Inicial | Tiempo | Complejidad |
|---------|-------------------|--------|-------------|
| **Validación Manual** | $0 | 2 semanas | Baja |
| **No-Code Prototype** | $0-50 | 2 semanas | Baja |
| **Low-Code MVP** | $500-800 | 4-6 meses | Media |
| **React Native MVP** | $700-1,000 | 6-8 meses | Alta |
| **Contratar Equipo** | $15,000-25,000 | 3-4 meses | Baja (para ti) |

**Recomendación para solo developer:**
```
1. Validación manual ($0, 2 semanas)
2. Si valida → Low-code MVP ($500-800, 4-6 meses)
3. Si funciona → Migrar a React Native o contratar dev
```

### 16.4 Presupuesto Realista Total (Año 1)

```
ESCENARIO CONSERVADOR:
Meses 1-2 (validación): $0-100
Meses 3-6 (desarrollo): $500-800
Meses 7-12 (operación): $1,350-3,150

TOTAL AÑO 1: $1,850 - 4,050 USD
(~ $33,000 - 73,000 MXN)

Con tu tiempo valorado a $0 (estás invirtiendo sweat equity)
```

```
ESCENARIO OPTIMISTA (Con Revenue):
Si alcanzas $65,000 MXN/mes en mes 12:
- Costos: $525/mes = $6,300/año
- Revenue año 1: ~$30,000 USD
- ROI: 741% 🎯
```

### 16.5 Cómo NO Gastar Demás

#### ✅ GASTA EN ESTO:
- Apple Developer ($99) - Necesario
- Google Play ($25) - Necesario
- GitHub Copilot ($10/mes) - 10x tu productividad
- Legal (T&C) ($200-300) - Protección esencial
- Dominio ($12) - Profesionalismo

#### ⚠️ TAL VEZ:
- Figma Pro ($15/mes) - Solo si diseñas mucho
- Cursor IDE ($20/mes) - Si Copilot no es suficiente
- Curso Udemy ($15) - Si eres principiante total
- Ads ($100-300) - Solo después de validar

#### ❌ NO GASTES (Al inicio):
- Servidor dedicado - Usa Firebase/Supabase
- Diseñador pro - Usa Figma + IA
- Copywriter - Usa ChatGPT
- Logo caro - Usa Canva ($30 max)
- Analytics pagado - Firebase es gratis
- CRM - Notion funciona
- Email marketing - 2,000 contacts gratis (Mailchimp)

**Regla de oro:** Gasta solo en lo que BLOQUEA tu progreso

### 16.6 Fuentes de Financiamiento

Si no tienes $500-1,000 USD iniciales:

**Opción 1: Bootstrapping**
```
- Ahorrar de tu trabajo 2-3 meses
- Freelance extra (Upwork, Fiverr)
- Vender algo que no uses
```

**Opción 2: Pre-ventas**
```
- Landing page con "early access"
- Ofrecer: "$99/año acceso lifetime"
- Meta: 10 pre-ventas = $990 cubre todo MVP
- Riesgo bajo, validas demanda
```

**Opción 3: Micro-préstamo**
```
- Familia/amigos: $500-1,000
- Prometes regresarlo en 6 meses
- Si falla, lo pagas de tu trabajo
```

**Opción 4: Fondos gubernamentales**
```
- INADEM (México) - Hasta $300,000 MXN
- Startup Mexico
- Aplicar lleva tiempo (3-6 meses)
- Solo si ya tienes tracción
```

**NO RECOMENDADO para MVP:**
- ❌ Inversionistas ángeles (muy temprano)
- ❌ Préstamos bancarios (riesgo innecesario)
- ❌ Tarjetas de crédito (intereses altos)

---

## 17. KPIs y Objetivos por Fase

### Fase 1: MVP (Mes 3)
```
✅ 500 usuarios registrados
✅ 100 transacciones completadas
✅ 30% tasa de conversión (subasta → venta)
✅ 4+ estrellas promedio en calificaciones
✅ <5% tasa de incidentes reportados
```

### Fase 1.5: Piloto Cupones (Mes 4)
```
✅ 5-10 PyMES activas
✅ 200+ cupones vendidos
✅ 80%+ tasa de redención
✅ 4+ estrellas promedio de usuarios
```

### Fase 2: Escalar (Mes 8)
```
✅ 2,000 usuarios activos
✅ 800 transacciones/mes
✅ 50+ PyMES en plataforma
✅ $20,000+ MXN en comisiones/mes
✅ 60% usuarios retornan en 30 días
```

### Fase 3: Optimización (Mes 12)
```
✅ 5,000 usuarios activos
✅ 2,000 transacciones/mes
✅ 100+ PyMES activas
✅ $65,000+ MXN en ingresos/mes
✅ Presencia en 3+ estados
✅ NPS > 50
```

---

## 22. Ejemplos de Prompts con Código (Para Usar con Claude)

### Guía de Uso

**Cada vez que pidas código a Claude:**
1. Menciona este documento: "Basado en contexto-app-subastas.md..."
2. Sé específico sobre el contexto (sección relevante)
3. Define claramente input/output esperado
4. Pide explicaciones si no entiendes algo

---

### Ejemplo 1: Autenticación con Teléfono

**Prompt:**
```
Basado en contexto-app-subastas.md sección 6.2 (estructura de usuarios),
genera el flujo completo de autenticación con teléfono en React Native:

Requisitos:
- Firebase Phone Authentication
- Pantalla 1: Input de teléfono (+52 MX)
- Pantalla 2: Input de código OTP (6 dígitos)
- Validación de formato
- Loading states
- Error handling
- Navegación a HomeScreen si éxito
- Guardar usuario en Firestore según esquema del documento

Usa:
- React Native
- Firebase v9+ (modular)
- React Navigation v6
- TypeScript
- react-hook-form para validación
```

**Resultado esperado:**
- Código de 2 componentes: PhoneInputScreen.tsx y OTPVerificationScreen.tsx
- Función de helper para Firebase Auth
- Manejo de errores específicos
- Comentarios explicativos

---

### Ejemplo 2: Crear Anuncio de Producto

**Prompt:**
```
Genera el componente CreateProductScreen basado en:
- Sección 6.2 del documento (estructura anuncios_productos)
- Solo 1 foto en MVP
- Categorías: Electrónica, Hogar, Ropa, Deportes, Otros

Features requeridos:
1. Upload de imagen desde galería o cámara
2. Form con campos:
   - Título (max 60 chars)
   - Descripción (max 500 chars)
   - Categoría (dropdown)
   - Precio mínimo (número, min $10)
   - Duración (opciones: 6h, 12h, 24h, 48h)
   - Zona de entrega (text input)
3. Validaciones con react-hook-form
4. Preview de imagen antes de subir
5. Loading durante upload
6. Upload a Firebase Storage
7. Guardar en Firestore con estructura del doc
8. Navegación a pantalla de confirmación

Usa TypeScript + React Native Paper para UI
```

---

### Ejemplo 3: Feed de Productos con Filtros

**Prompt:**
```
Crea ProductFeedScreen que muestre productos activos:

Basado en contexto-app-subastas.md sección 6.2 y 4.1:

Funcionalidad:
1. Fetch productos de Firestore donde:
   - estado_subasta = "activa"
   - ubicacion.municipio = usuario.municipio
   - fecha_fin > ahora
   - Ordenar por fecha_fin ASC (próximos a terminar primero)

2. Cada card muestra:
   - Imagen del producto
   - Título
   - Precio actual (última oferta o mínimo)
   - Tiempo restante (countdown en tiempo real)
   - Número de ofertas

3. Features:
   - Pull to refresh
   - Infinite scroll (paginación)
   - Loading skeleton
   - Empty state si no hay productos
   - Tap en card → navega a ProductDetailScreen

4. Filtros (botones arriba):
   - Todas las categorías
   - Solo "Electrónica"
   - Solo "Hogar"
   - etc.

Optimizar performance: solo cargar 20 productos inicialmente

Usa: FlatList, React Native Paper, Firestore queries
```

---

### Ejemplo 4: Sistema de Ofertas en Tiempo Real

**Prompt:**
```
Implementa sistema de ofertas para ProductDetailScreen:

Según contexto-app-subastas.md sección 6.2 (colección ofertas):

Componentes necesarios:
1. BidsList: Muestra ofertas actuales
2. PlaceBidButton: Botón para ofertar
3. BidModal: Modal para ingresar oferta

Lógica:
- Escuchar ofertas en tiempo real (Firestore onSnapshot)
- Ordenar por monto DESC
- Mostrar última oferta prominente
- Validaciones:
  * Nueva oferta > última oferta
  * Usuario no es el vendedor
  * Subasta aún activa
  * Monto >= precio_minimo
- Mostrar "Eres el ganador actual" si user tiene máxima oferta
- Al terminar countdown → automaticamente determinar ganador

Firestore operations:
- Leer: ofertas where anuncio_id
- Escribir: nueva oferta
- Transacciones para evitar race conditions

UI:
- Lista de ofertas con avatar, nombre, monto
- Input de monto con validación
- Animación al recibir nueva oferta
- Sonido opcional (react-native-sound)

TypeScript + error handling completo
```

---

### Ejemplo 5: Chat 1-a-1 Básico

**Prompt:**
```
Implementa chat simple entre comprador y vendedor:

Referencia: contexto-app-subastas.md secciones 6.2 (chats, mensajes)

Usa librería: @flyerhq/react-native-chat-ui

Funcionalidad:
1. ChatListScreen:
   - Lista de chats activos del usuario
   - Ordenar por último mensaje
   - Badge si hay no leídos
   - Preview último mensaje

2. ChatScreen:
   - Mensajes en tiempo real (Firestore)
   - Input para escribir
   - Enviar con Enter
   - Mostrar timestamp
   - Marcar como leído al abrir
   - Indicador de typing (opcional)

Estructura Firestore:
- Collection: chats
  * Participantes array
  * Último mensaje
  * Metadata
- SubCollection: messages
  * de_usuario_id
  * texto
  * fecha
  * leido boolean

Features adicionales:
- No permitir chat hasta que subasta termine
- Solo comprador ganador puede chatear
- Vendedor puede chatear con ganador

TypeScript + React Navigation
```

---

### Ejemplo 6: QR Dinámico para Cupones

**Prompt:**
```
Implementa sistema de QR dinámico descrito en 
contexto-app-subastas.md sección 7.1:

Lado Usuario (quien tiene cupón):
1. Screen MyCouponsScreen:
   - Lista de cupones activos
   - Filtros: activos, usados, expirados

2. Screen UseCouponScreen:
   - Mostrar detalles del cupón
   - Botón "Usar Ahora"
   - Al tocar:
     * Llamar Firebase Function: generateQRToken
     * Recibir token temporal
     * Generar QR con react-native-qrcode-svg
     * Mostrar countdown (180 segundos)
     * Detectar screenshot → invalidar token
     * Prevenir salir sin confirmar

Lado Negocio (scanner):
3. Screen ScanCouponScreen:
   - Usar react-native-camera para escanear
   - Leer QR
   - Llamar Firebase Function: validateQRToken
   - Mostrar resultado:
     * ✅ Válido: Info del cupón
     * ❌ Inválido: Razón del error

Firebase Functions:
4. generateQRToken:
   - Input: cupon_id, usuario_id
   - Validar: cupón existe, activo, pertenece a usuario
   - Generar token único (crypto)
   - Guardar en Firestore con TTL 180s
   - Return: token, expires_at

5. validateQRToken:
   - Input: token, negocio_id
   - Buscar token en Firestore
   - Validar: no expirado, negocio correcto
   - Marcar cupón como usado (atomic)
   - Eliminar token
   - Log de transacción
   - Return: success + coupon info

Incluye:
- TypeScript estricto
- Error handling exhaustivo
- UI con React Native Paper
- Animaciones suaves
```

---

### Ejemplo 7: Sistema de Calificaciones

**Prompt:**
```
Crear sistema de calificaciones mutuas post-transacción
según contexto-app-subastas.md sección 7.2:

Flow:
1. Después de entrega → Ambos usuarios ven "Calificar"
2. RatingScreen:
   - Rating 1-5 estrellas (react-native-ratings)
   - 4 aspectos para vendedor:
     * Descripción precisa
     * Puntualidad
     * Estado del producto
     * Amabilidad
   - 3 aspectos para comprador:
     * Puntualidad
     * Pago correcto
     * Trato respetuoso
   - Comentario opcional (300 chars max)
   - Botón submit

3. Guardar en Firestore:
   - Collection: calificaciones
   - Actualizar promedio en documento usuario
   - No permitir editar después

4. Mostrar en perfil:
   - Promedio general
   - Número de calificaciones
   - Comentarios recientes (últimos 5)
   - Badge si >4.5 estrellas

Features:
- No permitir calificar dos veces
- Ambos deben calificar para ver la del otro
- Notificación recordatorio después de 24h
- Reportar calificación inapropiada

TypeScript + validaciones
```

---

### Ejemplo 8: Refactorizar Código Existente

**Prompt:**
```
Tengo este componente que funciona pero es difícil de mantener:

[PEGAR CÓDIGO AQUÍ]

Problemas:
- Lógica mezclada con UI
- No usa custom hooks
- Muchos useEffect
- No tiene loading/error states
- Difícil de testear

Refactoriza siguiendo:
1. Separar lógica en custom hooks
2. Componente solo UI
3. Añadir tipos TypeScript
4. Error boundary
5. Loading skeletons
6. Comentarios explicativos
7. Seguir atomic design si posible

Mantener funcionalidad exacta pero mejor estructura.
Explica cada cambio importante que hiciste.
```

---

### Ejemplo 9: Debugging de Error Específico

**Prompt:**
```
Tengo este error en producción:

Error: [PEGAR ERROR COMPLETO CON STACK TRACE]

Contexto:
- Ocurre en: [pantalla/función]
- Cuando usuario: [acción específica]
- Datos involucrados: [ejemplo de data]
- Ya intenté:
  1. [intento 1]
  2. [intento 2]
  
Código relevante:
[PEGAR CÓDIGO]

Necesito:
1. Explicación de por qué ocurre
2. Solución paso a paso
3. Código corregido
4. Cómo prevenir en futuro
5. Test case para este escenario

Proyecto: React Native + Firebase según contexto-app-subastas.md
```

---

### Ejemplo 10: Agregar Feature Nueva

**Prompt:**
```
Necesito agregar feature: [DESCRIPCIÓN]

Contexto del proyecto: [referir a sección específica del doc]

Requiero:
1. Análisis de impacto:
   - Qué componentes afecta
   - Qué datos necesita
   - Cambios en Firestore
   - Nuevos endpoints si aplica

2. Propuesta de implementación:
   - Estructura de componentes
   - Nuevos hooks necesarios
   - Cambios en navegación
   - Actualizaciones de tipos

3. Código completo:
   - Nuevos archivos
   - Modificaciones a existentes
   - Tests básicos
   - Comentarios

4. Consideraciones:
   - Performance
   - Seguridad
   - UX
   - Backwards compatibility

Prioriza simplicidad y mantenibilidad.
```

---

### Tips para Prompts Efectivos

**✅ HACER:**
- Ser específico sobre el contexto
- Incluir requisitos técnicos (libs, patterns)
- Pedir explicaciones junto con código
- Mencionar restricciones o limitaciones
- Dar ejemplos de input/output
- Pedir TypeScript + validaciones

**❌ EVITAR:**
- Prompts vagos: "crea una app de subastas"
- Sin contexto del stack tecnológico
- Pedir múltiples features complejas juntas
- No especificar tipos de datos
- Olvidar edge cases

**FÓRMULA GANADORA:**
```
1. Contexto: "Basado en [sección del doc]..."
2. Objetivo: "Necesito [feature X] que [hace Y]"
3. Requisitos: "Debe incluir [lista]"
4. Stack: "Usa [tecnologías]"
5. Output: "Dame [código + explicación + tests]"
```

---

### Manteniendo Conversación con Claude

**Para desarrollos largos:**

1. **Inicio de sesión:**
```
"Hola, trabajaré hoy en [feature]. 
Por favor lee contexto-app-subastas.md 
sección [X] para contexto completo."
```

2. **Durante desarrollo:**
```
"Anteriormente generaste [componente X].
Ahora necesito [modificación Y] que 
se integre con lo anterior..."
```

3. **Revisión de código:**
```
"Revisa el código que acabas de generar:
- ¿Hay vulnerabilidades de seguridad?
- ¿Está optimizado?
- ¿Faltan validaciones?
- ¿Cumple con best practices React Native?"
```

4. **Documentación:**
```
"Genera README.md para este componente
que explique:
- Propósito
- Props
- Cómo usar
- Ejemplos
- TODOs pendientes"
```

---

### Cuando Pedir Ayuda vs. Investigar Solo

**Pide ayuda a Claude si:**
- ✅ Llevas >1 hora atascado
- ✅ No entiendes error o concepto
- ✅ Necesitas refactorizar código complejo
- ✅ Quieres segunda opinión sobre arquitectura
- ✅ Buscas mejores prácticas

**Investiga solo primero si:**
- ⚠️ Error tiene stack trace claro
- ⚠️ Problema de sintaxis simple
- ⚠️ Documentación oficial cubre el tema
- ⚠️ Es cuestión de configuración

**Equilibrio:** Usa IA para acelerar, pero entiende el código que generas

---

### Q: ¿Por qué solo efectivo en MVP?
A: Simplifica dramáticamente el desarrollo y reduce riesgos legales/financieros. Integrar pasarelas de pago requiere compliance, costos de transacción y complejidad técnica innecesaria para validación inicial.

### Q: ¿Por qué subastas en lugar de precio fijo?
A: Genera mayor engagement, emoción y sentido de urgencia. El formato gamifica la experiencia y puede lograr mejores precios tanto para vendedores (demanda alta) como compradores (oportunidades).

### Q: ¿Cómo compite con Facebook Marketplace?
A: Diferenciadores clave: (1) Formato subasta temporal, (2) Subastas privadas entre conocidos, (3) Cupones de PyMES locales, (4) Enfoque 100% local sin envíos, (5) Estructura profesional vs spam de FB.

### Q: ¿Qué pasa si un usuario no paga/entrega?
A: Sistema de calificaciones hace visible el historial. Usuarios con malas calificaciones son menos confiables. En fase 2, podemos agregar sistema de depósito/garantía.

### Q: ¿Cómo evitar que compartan QR de cupones?
A: QR dinámico que se genera solo cuando usuario está listo para usar, expira en 3 minutos, es único por sesión, se invalida al usarse una vez, y detecta screenshots.

### Q: ¿Por qué PyMES pagarían por usar la app?
A: No pagan hasta que venden (comisión) o eligen plan premium. ROI claro: llenan horarios muertos, consiguen clientes nuevos, marketing más barato que Google Ads, control total sobre sus promociones.

### Q: ¿Qué evita que competencia copie la idea?
A: Ejecución rápida, comunidad fuerte, network effects (más usuarios = más valor), relaciones con PyMES locales, know-how de operación, marca y confianza. Ideas son baratas, ejecución lo es todo.

---

## 19. Próximos Pasos Recomendados

### Inmediato (Próximas 2 semanas)
1. ✅ Validar con encuestas:
   - 50 usuarios potenciales: ¿Usarían la app?
   - 20 PyMES: ¿Subastarían cupones?
2. ✅ Crear landing page simple
3. ✅ Empezar captación de emails
4. ✅ Definir presupuesto disponible
5. ✅ Decidir: ¿Equipo interno o outsourcing?

### Corto Plazo (1 mes)
1. ✅ Contratar/armar equipo de desarrollo
2. ✅ Wireframes y diseño UI/UX
3. ✅ Setup de infraestructura (Firebase)
4. ✅ Redactar T&C y política de privacidad
5. ✅ Contactar primeras 10 PyMES para piloto

### Mediano Plazo (3 meses)
1. ✅ Desarrollo de MVP
2. ✅ Beta testing con usuarios cerrados
3. ✅ Iteración basada en feedback
4. ✅ Preparar materiales de marketing
5. ✅ Lanzamiento suave

---

## 20. Contacto y Mantenimiento del Documento

**Versión:** 1.0  
**Última actualización:** Octubre 31, 2025  
**Próxima revisión:** Post-MVP (Mes 4)

**Propósito de este documento:**
Servir como base de conocimiento para cualquier herramienta de IA o miembro del equipo que trabaje en el proyecto. Contiene decisiones de diseño, arquitectura, restricciones y contexto completo de la visión del producto.

**Actualizaciones futuras deberían incluir:**
- Feedback de usuarios reales
- Pivots o cambios de estrategia
- Nuevas funcionalidades validadas
- Métricas reales vs proyectadas
- Learnings y experimentos

---

## Apéndice A: Decisiones Clave del Diseño

### 1. ¿Por qué React Native y no nativo?
- **Pros:** Desarrollo más rápido, un equipo para iOS y Android, reducción de costos 50%
- **Contras:** Menor performance en animaciones complejas (no crítico para MVP)
- **Decisión:** React Native para MVP, posible migración a nativo si se valida el producto

### 2. ¿Por qué Firebase y no backend custom?
- **Pros:** Setup rápido, serverless, escalabilidad automática, SDKs robustos, menor costo inicial
- **Contras:** Vendor lock-in, costos crecen con escala
- **Decisión:** Firebase para MVP, evaluar migración si alcanzamos escala significativa

### 3. ¿Por qué no incluir envíos en MVP?
- **Razones:** Complejidad logística, costos, responsabilidades legales, validar concepto core primero
- **Alternativa:** Enfoque 100% local elimina esta necesidad
- **Futuro:** Agregar alianza con mensajería en Fase 3

### 4. ¿Por qué QR dinámico vs estático?
- **Razones:** Prevenir fraude, compartir screenshots, reventa de cupones, uso múltiple
- **Costo:** Ligeramente más complejo técnicamente pero crucial para seguridad
- **Resultado:** Vale la complejidad extra desde día 1

### 5. ¿Por qué empezar con un solo municipio?
- **Razones:** Más fácil generar densidad de red, marketing enfocado, logística simple, iterar rápido
- **Estrategia:** Dominar local antes de expandir
- **Meta:** 1,000 usuarios en un municipio vale más que 100 usuarios en 10 municipios

---

## Apéndice B: Glosario de Términos

- **MVP:** Minimum Viable Product (Producto Mínimo Viable)
- **PyME:** Pequeña y Mediana Empresa
- **GMV:** Gross Merchandise Value (Valor Bruto de Mercancía transaccionada)
- **DAU/MAU:** Daily/Monthly Active Users (Usuarios Activos Diarios/Mensuales)
- **NPS:** Net Promoter Score (Métrica de satisfacción del cliente)
- **TTL:** Time To Live (Tiempo de vida de un token/dato)
- **LTV:** Lifetime Value (Valor de vida del cliente)
- **Churn:** Tasa de abandono de usuarios
- **K-factor:** Coeficiente de viralidad
- **Freemium:** Modelo de negocio con versión gratuita y premium
- **QR Dinámico:** Código QR que se genera temporalmente vs. permanente

---

## Apéndice C: Referencias y Recursos

### Inspiración de Producto
- eBay: Pionero en subastas online
- Wallapop: UX simple para segunda mano
- Groupon: Modelo de cupones de descuento
- Nextdoor: Enfoque hiperlocal de comunidad
- Vinted: Sistema de envíos y pagos seguros

### Stack Técnico
- React Native: https://reactnative.dev/
- Firebase: https://firebase.google.com/
- Expo: https://expo.dev/
- React Native QR: https://github.com/cssivision/react-native-qrcode-svg

### Regulación (México)
- LFPDPPP: Ley Federal de Protección de Datos Personales en Posesión de Particulares
- PROFECO: Procuraduría Federal del Consumidor
- Comercio Electrónico: https://www.gob.mx/profeco

### Herramientas de Análisis
- Mixpanel: Product analytics
- Firebase Analytics: Comportamiento usuarios
- Hotjar: Heatmaps y session recordings (web)

---

## 21. Plan de Acción Paso a Paso (Solo Developer)

### Tu Roadmap Personal de Ejecución

#### 🎯 SEMANA 1: Validación Rápida

**Lunes:**
- [ ] Crear Google Form con 10 preguntas clave
- [ ] Compartir en 5 grupos de Facebook/WhatsApp
- [ ] Target: 20 respuestas

**Martes-Miércoles:**
- [ ] Llamar/visitar 5 PyMES locales
- [ ] Pitch de 2 minutos: "App para subastar cupones"
- [ ] Anotar objeciones y preguntas

**Jueves-Viernes:**
- [ ] Analizar resultados
- [ ] Decidir: GO / NO-GO / PIVOT
- [ ] Si GO: Crear landing page (Carrd.co - gratis)

**Sábado-Domingo:**
- [ ] Diseñar mockups básicos en Figma (3-4 pantallas)
- [ ] Escribir user stories principales
- [ ] Leer este documento completo

**Inversión:** $0 | **Tiempo:** 15-20 horas

---

#### 🎯 SEMANA 2: Setup y Aprendizaje

**Si no conoces React Native:**
- [ ] Ver crash course YouTube (4 horas)
- [ ] Tutorial oficial Expo (6 horas)
- [ ] Hacer app "Hello World" y deployar

**Setup de Herramientas:**
- [ ] Instalar VS Code + GitHub Copilot
- [ ] Crear cuenta Firebase/Supabase
- [ ] Setup repositorio GitHub
- [ ] Instalar React Native + Expo
- [ ] Configurar emulador iOS/Android

**Arquitectura:**
- [ ] Usar Claude para generar estructura de proyecto
- [ ] Definir estructura de carpetas
- [ ] Setup navegación básica

**Inversión:** $10 (Copilot) | **Tiempo:** 20-25 horas

---

#### 🎯 SEMANAS 3-6: MVP Core (Productos Solo)

**Semana 3: Auth + Perfil**
```
- [ ] Screen: Login con teléfono
- [ ] Integración Firebase Auth (OTP)
- [ ] Screen: Completar perfil
- [ ] Selección de ubicación
- [ ] Guardar usuario en Firestore

Prompt para Claude:
"Basado en contexto-app-subastas.md sección 6.2,
genera el flujo completo de autenticación con 
Firebase Phone Auth en React Native. Incluye..."
```

**Semana 4: Crear/Ver Productos**
```
- [ ] Screen: Crear anuncio
- [ ] Upload foto (1 por ahora)
- [ ] Form con validación
- [ ] Guardar en Firestore
- [ ] Screen: Feed de productos
- [ ] Filtro por municipio

Prompt para Claude:
"Genera componente CreateProductScreen con:
- Upload de imagen a Firebase Storage
- Form usando react-hook-form
- Validaciones de precio, descripción, etc..."
```

**Semana 5: Ofertas y Subasta**
```
- [ ] Screen: Detalle de producto
- [ ] Botón "Hacer oferta"
- [ ] Validar oferta > última
- [ ] Guardar oferta en Firestore
- [ ] Lista de ofertas en tiempo real
- [ ] Countdown timer de subasta

Prompt para Claude:
"Sistema de ofertas en tiempo real usando
Firestore onSnapshot. Incluir validación
de que oferta actual > máxima anterior..."
```

**Semana 6: Chat Básico**
```
- [ ] Screen: Lista de chats
- [ ] Screen: Chat 1-a-1
- [ ] Enviar/recibir mensajes
- [ ] Integración Firestore
- [ ] Notificaciones (básico)

Usar librería: @flyerhq/react-native-chat-ui

Prompt para Claude:
"Implementar chat usando Firestore y
la librería react-native-chat-ui.
Estructura de datos según documento..."
```

**Inversión:** $200 (Firebase + tools) | **Tiempo:** 60-80 horas

---

#### 🎯 SEMANAS 7-8: Polish y Testing

**Semana 7: UI/UX**
```
- [ ] Agregar React Native Paper
- [ ] Mejorar navegación
- [ ] Estados de loading
- [ ] Error handling
- [ ] Pantalla de vacío
- [ ] Splash screen

Prompt para Claude:
"Audita estas 5 pantallas y sugiere
mejoras de UX siguiendo Material Design..."
```

**Semana 8: Testing**
```
- [ ] Reclutar 10 beta testers (amigos)
- [ ] Crear grupo WhatsApp de beta
- [ ] Deployar con Expo EAS
- [ ] Recolectar bugs en Notion
- [ ] Fix bugs críticos
- [ ] Iterar basado en feedback

No usar prompt - trabajo manual
```

**Inversión:** $0 | **Tiempo:** 30-40 horas

---

#### 🎯 SEMANA 9-10: Lanzamiento Suave

**Pre-Lanzamiento:**
```
- [ ] Registrar en Apple/Google
- [ ] Crear assets (screenshots, description)
- [ ] Preparar T&C y Privacy Policy
- [ ] Setup analytics
- [ ] Crear perfiles en redes
```

**Lanzamiento:**
```
- [ ] Invitar primeros 50 usuarios
- [ ] Monitorear errores 24/7
- [ ] Responder feedback
- [ ] Fix bugs urgentes
- [ ] Documentar learnings
```

**Inversión:** $124 (Apple+Google) | **Tiempo:** 30-40 horas

---

### Checklist Diario de Desarrollo

**Cada día que trabajes:**

```
Antes de empezar:
[ ] Revisar issues/bugs de ayer
[ ] Priorizar top 3 tareas del día
[ ] Abrir este documento + contexto

Durante desarrollo:
[ ] Commit cada feature completo
[ ] Comentar código complejo
[ ] Testear en emulador
[ ] Escribir prompt específico para IA

Antes de terminar:
[ ] Push a GitHub
[ ] Actualizar Notion/Trello
[ ] Anotar blockers para mañana
[ ] 5 min de reflection: ¿qué aprendí?
```

### Prompts Específicos por Tarea

#### 1. Cuando empiezas una feature nueva:
```
"Voy a implementar [FEATURE].

Contexto del proyecto: [pegar sección relevante de este doc]

Dame:
1. Estructura de componentes recomendada
2. Código inicial con TypeScript
3. Puntos que debo considerar
4. Posibles problemas y soluciones

Usa: React Native, Firebase, React Navigation, TypeScript"
```

#### 2. Cuando tienes un bug:
```
"Tengo un bug:

Error: [mensaje de error completo]

Código relevante:
[pegar código]

Qué intenté:
1. [intento 1]
2. [intento 2]

Qué debería hacer: [comportamiento esperado]
Qué hace: [comportamiento actual]

¿Cuál es el problema y cómo lo soluciono?"
```

#### 3. Cuando necesitas refactorizar:
```
"Este código funciona pero es difícil de mantener:

[pegar código]

Refactoriza siguiendo:
- Clean code principles
- React best practices
- TypeScript strict
- Comentarios explicativos

Y explica qué cambiaste y por qué."
```

#### 4. Cuando necesitas optimizar:
```
"Esta pantalla es lenta:

[describir pantalla y código]

Usuario experimenta: [problema de performance]

Analiza y dame:
1. Causas probables
2. Soluciones priorizadas por impacto
3. Código optimizado
4. Cómo medir la mejora"
```

#### 5. Cuando necesitas integrar algo nuevo:
```
"Necesito integrar [librería/servicio].

Propósito: [qué quieres lograr]
Restricciones: [limitaciones]

Dame:
1. Mejores opciones (librerías)
2. Pros y contras de cada una
3. Código de integración
4. Configuración necesaria
5. Costos si aplica"
```

### Recursos de Emergencia

#### Si te atoras más de 2 horas:
1. Pausa 15 minutos - sal a caminar
2. Explica el problema a Claude como si fuera un colega
3. Busca en Stack Overflow
4. Revisa GitHub Issues de la librería
5. Pregunta en Discord de React Native
6. Si nada funciona: implementa workaround temporal

#### Comunidades de Ayuda:
- React Native Discord
- r/reactnative (Reddit)
- Stack Overflow (tag: react-native)
- Expo Discord
- Firebase Discord

#### Cuando considerar contratar ayuda:
- ✅ Atascado >1 semana en mismo problema
- ✅ Feature crítico muy complejo
- ✅ Bug en producción que afecta usuarios
- ✅ Necesitas expertise específico (ej: seguridad)

**Costo:** $50-150/hora en Upwork para consultoría puntual

### Métricas Personales a Trackear

**Cada semana anota:**
```
✅ Features completados: [#]
🐛 Bugs arreglados: [#]
⏱️ Horas invertidas: [#]
📚 Cosas nuevas aprendidas: [lista]
😊 Nivel de satisfacción: [1-10]
💰 Gasto de la semana: [$]

🎯 Próxima semana:
- Objetivo principal: [definir]
- 3 tareas clave: [listar]
```

### Señales de que Vas Bien

```
✅ Cada semana hay algo funcional nuevo
✅ Bugs están disminuyendo, no aumentando
✅ Te sientes más cómodo con el stack
✅ El código de la semana pasada tiene sentido
✅ Resuelves problemas más rápido
✅ Beta testers dan feedback positivo
✅ Te emociona mostrar el progreso
```

### Señales de Alerta

```
🚩 Semanas sin progreso visible
🚩 Reescribes todo constantemente
🚩 No entiendes tu propio código
🚩 Bugs se multiplican
🚩 Dejaste de disfrutarlo
🚩 Nadie usa el beta
🚩 Presupuesto se acabó

Acción: Reevaluar, pedir ayuda, o pivotar
```

---

**FIN DEL DOCUMENTO**

*Este documento es un living document que debe evolucionar con el producto. Mantenerlo actualizado es crucial para el éxito del proyecto.*
