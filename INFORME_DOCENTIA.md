# Docentia — Informe Completo para Hermes

**Generado por:** Newen 🚀  
**Para:** Hermes — Asistente Personal de Cristian Iglesias Vera  
**Fecha:** 2026-05-18

---

## 1. ¿Qué es Docentia?

Docentia es una plataforma de inteligencia artificial aplicada a la educación superior, fundada y liderada por Cristian Iglesias Vera. Su misión es **democratizar el acceso a la IA en la docencia universitaria**, proporcionando a los profesores un equipo de agentes especializados que asisten en todas las áreas de la labor docente.

**Sitio web:** https://docentia.skylabs.cl

**Visión (texto del sitio):** "84% de la población mundial nunca ha usado IA. Docentia existe para cambiar eso, empezando por las aulas universitarias."

---

## 2. Arquitectura del equipo

Docentia funciona con un modelo de **agentes especializados** orquestados por un líder:

```
Newen 🚀 (Líder / Orquestador)
│
├── Adkintun 👁️ — Diseño Curricular
├── Ayekan 🧠 — Psicología Educativa (NEE, inclusión)
├── Kümeelkan ✅ — Evaluación y Feedback
├── Kintun 📊 — Administrativo (notas, asistencia, actas)
├── Pewma 💬 — Apoyo Estudiantil (atención 24/7)
├── Wirin 🎨 — Generador de Contenidos (materiales didácticos)
└── Kallfü 📈 — Analista de Datos (dashboards, predicciones)
```

Cada agente tiene:
- **Identidad propia:** nombre en mapudungun, personalidad definida en SOUL.md
- **Skills especializadas:** scripts Python con herramientas específicas
- **Acceso al repositorio:** lectura de docentia-docs vía skill compartida
- **Modelo LLM:** deepseek-v4-pro (agentes principales) o v4-flash (agentes ligeros)

---

## 3. Proyectos activos

### 3.1 TINF1113 — Desarrollo y Diseño Web + IA (UCT)

**Cliente:** Cristian Iglesias como docente UCT  
**Estado:** En curso (marzo - julio 2026)  
**Estudiantes:** ~36 en 2 secciones (S1: 18, S2: 17)  

**Entregables generados:**
- Evaluación N°2 (Abril 2026): 34 estudiantes evaluados con rúbrica automatizada
- Presentaciones semanales: semanas 8, 9, 10, 12, 13 generadas con plantilla TECUCT
- Actividades autónomas, guías de laboratorio, ejercicios prácticos

**Ajustes CERETI activos:**
- Felipe Salazar (S2): TEA, criterios simplificados
- Cristóbal Cisterna (S2): Dificultades de aprendizaje, plazo extendido
- Vicente Ortiz (S1): 50% tiempo extra
- Benjamín Alegría (S1): Dificultades de aprendizaje
- Antonio Carrasco (S2): TDAH

**Semana más reciente:** Semana 9 (AJAX/JSON, fetch(), PHP backend, Bootstrap)

### 3.2 IA Executive — Skillnest

**Cliente:** Skillnest (antes Coding Dojo Latam)  
**Rol de Cristian:** Relator del curso  
**Estado:** Materiales generados, curso inició 12 mayo 2026  
**Duración:** 11 semanas, 22 sesiones  

**Entregables generados:**
- Guía docente completa (22 sesiones) en `skillnest/guia_docente_ia_executive.md`
- Material Sesión 1 y 2 (guion instructor, slides, demos, actividades)
- Kit de 20 plantillas de prompt ejecutivo
- Sistema de evaluación (3 rúbricas, guía de proyecto, checklist)

### 3.3 Constructora KC — Dashboard de Marketing

**Cliente:** Karim Cueto (Constructora KC)  
**Dominio:** www.proyectoskc.cl  
**Repositorio:** github.com/admrrsscl-debug/constructora-karim-web  
**Hosting:** DirectAdmin  
**Estado:** Dashboard construido, pendiente despliegue final  

**Sistema implementado:**
- Funnel de marketing TOFU → MOFU → BOFU
- Admin dashboard (/admin/) con Google Sign-In
- Cliente dashboard (/mi-cuenta/) con magic link
- Automatización: emails (SMTP), cotizador, agendamiento (Google Calendar)

**Base de datos:** `proyectoskc_funnel` en DirectAdmin

### 3.4 Agent Town — Oficina Virtual

**URL local:** http://localhost:3001  
**Tecnología:** Next.js + Phaser.js (2D tile map)  
**Función:** Visualización de los agentes Docentia en un mapa de oficina virtual  

**Configuración:**
- Gateway proxy en `/api/gateway`
- 9 agentes visibles (Newen + 7 especialistas + Kimche)
- Conexión WebSocket: `ws://127.0.0.1:18789/`
- Token gateway configurado

---

## 4. Repositorios

| Repo | URL | Propietario | Contenido |
|---|---|---|---|
| docentia-docs | github.com/ciglesiasvera/docentia-docs | Cristian | Material curso UCT, estudiantes, rúbricas, CERETI |
| constructora-karim-web | github.com/admrrsscl-debug/constructora-karim-web | Newen/Cristian | Sitio proyectoskc.cl, dashboard, funnel |
| config-hermes | github.com/admrrsscl-debug/config-hermes | Newen | Archivos de configuración para Hermes |
| spec-kit | github.com/github/spec-kit | GitHub (OSS) | Metodología Spec-Driven Development |
| superpowers | github.com/obra/superpowers | Jesse Vincent | Skills framework para agentes IA |
| agent-town | github.com/geezerrrr/agent-town | Tercero (OSS) | Oficina virtual 2D |

---

## 5. Metodología: Spec-Driven Development

Docentia adoptó y consolidó la metodología de desarrollo basada en especificaciones, combinando:

- **Spec Kit** (github/spec-kit): Spec-Driven, ciclo Specify → Plan → Tasks → Implement
- **Superpowers** (obra/superpowers): TDD, subagent-driven, skills automáticas
- **Discovery → Delivery** (Javier Garzas): Separar entendimiento de implementación

### Estructura de archivos de cada proyecto:
```
especificaciones/[proyecto]/
├── spec.md       ← QUÉ y POR QUÉ (problema, contexto, criterios de aceptación)
├── plan.md       ← CÓMO (stack, arquitectura, validación)
└── tasks.md      ← Desglose de tareas atómicas (2-5 min c/u)
```

### Principios:
1. Spec-First: no construir sin spec aprobado
2. TDD: RED → GREEN → REFACTOR siempre
3. YAGNI: solo lo que pide el spec
4. Evidencia sobre afirmaciones
5. Tareas atómicas de 2-5 minutos
6. Un agente por tarea (subagent-driven)
7. Discovery → Delivery: no mezclar fases

---

## 6. Infraestructura técnica

### Google Cloud (newenbot)
- **Proyecto GCP:** newenbot (ID: 991872367770)
- **Cuenta OAuth:** adm.rrss.cl@gmail.com
- **APIs habilitadas:** Drive, Slides, Docs, Sheets
- **API pendiente:** Calendar
- **Token:** `/home/dev/.openclaw/google-token.pickle`

### Modelos LLM
- **Principal:** deepseek-v4-pro (Newen, Adkintun, Ayekan, Kümeelkan, Wirin, Kallfü)
- **Ligero:** deepseek-v4-flash (Kintun, Pewma, Kimche)
- **Razonamiento:** deepseek-reasoner (disponible, poco usado)

### Servidores
- **Linux (Newen):** Ubuntu, host de desarrollo principal
- **Windows 10 (Hermes/Antu):** PC de Cristian, desarrollo con VS Code
- **DirectAdmin:** Hosting producción (proyectoskc.cl)

### Comunicación
- **Telegram:** principal, configurado con bot token
- **WhatsApp:** secundario, número +56985710670
- **TTS:** Microsoft Edge TTS, voz Lorenzo (es-CL-LorenzoNeural)

---

## 7. Estado actual (18 mayo 2026)

### ✅ Completado
- Evaluación N°2 UCT
- Semana 8-13 presentaciones UCT
- Semana 9: contenido completo + slides generados
- Dashboard Constructora KC (admin + cliente)
- Funnel TOFU/MOFU/BOFU implementado
- Spec-Driven Development consolidado
- Archivos de configuración para Hermes generados
- Esquema BD desplegado en DirectAdmin

### 🔴 Pendiente urgente
- Slides IA Executive S1 y S2 en Google Slides
- Probar SMTP con `info@proyectoskc.cl` en DirectAdmin
- Agregar scope Calendar al token OAuth
- Desplegar landing funnel en producción (proyectoskc.cl)

### 🟡 Pendiente normal
- Semanas 10, 11, 14, 15 UCT (cuando Cristian las solicite)
- Agent Town: personalizar mapa con marca Docentia
- Informe para Nicole Maldonado (CERETI)
- Re-evaluar Cristóbal Cisterna (plazo 18 mayo — ¡hoy!)
- PPTX export de presentaciones Semana 9

---

## 8. Coordinación Newen ↔ Hermes

**Newen (Linux):**
- Orquestador de los 7 agentes Docentia
- Acceso a Google APIs (Drive, Slides, Docs)
- Scripts de automatización (Python)
- Generación de presentaciones con Google Slides API
- Evaluación automatizada con rúbricas

**Hermes (Windows):**
- Asistente personal directo de Cristian
- Desarrollo en VS Code
- Coordinación con Newen para tareas que requieran infraestructura Linux
- Acceso a los mismos repositorios y documentación

**Flujo de trabajo entre ambos:**
1. Cristian pide algo a Hermes (Windows)
2. Hermes crea spec + plan
3. Si la tarea requiere Google APIs o agentes Docentia → Hermes coordina con Newen
4. Newen ejecuta la parte técnica, devuelve resultado
5. Hermes integra y presenta a Cristian

---

*Informe generado para Hermes. Actualizado al 18 de mayo de 2026.*
