# AGENTS.md — Reglas de Trabajo de Hermes

## 🚨 REGLA #1 — IDIOMA

**ESPAÑOL CHILENO O NEUTRO. JAMÁS ARGENTINO.**

Palabras PROHIBIDAS y sus reemplazos:

| ❌ NUNCA usar | ✅ Usar siempre |
|---|---|
| tenés, necesitás, podés, sabés, querés, pensás | tienes, necesitas, puedes, sabes, quieres, piensas |
| hablás, entendés, conocés, recordás, dejás | hablas, entiendes, conoces, recuerdas, dejas |
| decís, sentís, escribís, pedís, salís, venís | dices, sientes, escribes, pides, sales, vienes |
| andá, hacé, poné, decí, salí, vení | ve, haz, pon, di, sal, ven |

**Antes de CADA respuesta, revisar la columna izquierda. Si hay match → reemplazar.**

---

## Metodología de trabajo: Spec-Driven Development

### El ciclo (NUNCA te saltes un paso)

```
DISCOVERY:  BRAINSTORMING → SPECIFY  (spec.md)
DELIVERY:   PLAN → TASKS → IMPLEMENT → REVIEW  (plan.md, tasks.md)
```

### Los 3 archivos

| Archivo | Pregunta que responde | Crear |
|---|---|---|
| `spec.md` | ¿QUÉ y POR QUÉ? | PRIMERO |
| `plan.md` | ¿CÓMO? | SEGUNDO |
| `tasks.md` | ¿En qué orden? | TERCERO |

### Reglas de oro
- **Spec-First:** Sin spec aprobado, no se escribe código
- **TDD:** RED → GREEN → REFACTOR siempre
- **YAGNI:** No construyas lo que no pidieron
- **Tareas de 2-5 min:** Atómicas, un verbo, un archivo, un criterio
- **Un commit por tarea completada**

---

## Evaluación (modo docente UCT)

### Rúbrica estándar TINF1113
- S1: HTML(20), CSS(20), JS(20), BP(10), IA(10), EO(10), GIT(10) = 100 pts
- Fórmula: Nota = 4.0 + (Puntos - 60) × 0.075 (mín 1.0, máx 7.0)

### Reglas de evaluación
- Solo penalizar lo que está EXPLÍCITAMENTE en la rúbrica
- localStorage NO está en la rúbrica → NO penalizar
- Aplicar ajustes CERETI ANTES de evaluar
- Misma rúbrica para todos en una sección
- Diferenciar solo con ajustes razonables documentados
- Cada nota debe ser defendible con evidencia del repositorio

---

## Presentaciones (modo diseño curricular)

### Método definitivo (Google Slides API)
1. Copiar plantilla TECUCT en Drive (T1 para impares, T2 para pares)
2. Eliminar slides sobrantes
3. Reemplazar SOLO texto en shapes existentes (deleteText + insertText)
4. NUNCA sobrescribir logos ni imágenes
5. Verificar: 0 Lorem, 0 "Tarapacá", ≥1 imagen en portada

### Plantillas TECUCT en Drive
- TECUCT 1: 1-8Yq2qszD-sA4uXQFRAMYUP2_lTH5FiZAQ3kSD1ZyLQ
- TECUCT 2: 1lvHQXD6hldAh4PnheOw1ooTQ2TJufPtmR-8bB2rgzEI

### Layouts disponibles
p20=TITLE, p21=OBJECT, p22=SECTION_HEADER, p23=TWO_OBJECTS, 
p24=TWO_OBJECTS_WITH_TEXT, p25=TITLE_ONLY, p26=BLANK,
p27=OBJECT_WITH_CAPTION_TEXT, p28=PICTURE_WITH_CAPTION_TEXT

---

## Google APIs (para Cristian)

### Token OAuth
- Cuenta: adm.rrss.cl@gmail.com
- Proyecto GCP: newenbot (ID: 991872367770)
- Token: /home/dev/.openclaw/google-token.pickle
- Credenciales: /home/dev/.openclaw/google-oauth.json
- Scopes activos: Drive, Slides, Docs, Sheets
- Scope pendiente: Calendar (reautorizar para agregarlo)

---

## Repositorios de Cristian

| Repo | URL | Propósito |
|---|---|---|
| docentia-docs | github.com/ciglesiasvera/docentia-docs | Material UCT |
| constructora-karim-web | github.com/admrrsscl-debug/constructora-karim-web | Sitio proyectoskc.cl |

---

## Herramientas y entornos

- **TTS:** Voz Lorenzo (es-CL-LorenzoNeural, Microsoft Edge TTS)
- **Slides:** Google Slides API (NO python-pptx directo)
- **Código:** HTML5 + CSS3 + Bootstrap 5.3 + JS vanilla + PHP 8 + MySQL
- **IA:** Google Gemini, Notebook LM, Claude AI
- **Metodología:** github/spec-kit + obra/superpowers + Discovery/Delivery

---

## Referencias rápidas

- Spec Kit: https://github.com/github/spec-kit
- Superpowers: https://github.com/obra/superpowers
- Metodología completa: `.speckit/METODOLOGIA.md`
- Principios: `.speckit/constitution.md`
- Prompt Hermes: `.speckit/PROMPT_ANTU.txt`
