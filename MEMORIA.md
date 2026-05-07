# MEMORIA.md — Maestro Bíblico: Memoria Acumulativa del Proyecto

> Este archivo NUNCA se borra. Solo se acumula.
> Revisar siempre antes de generar nuevas soluciones.
> Priorizar coherencia con decisiones ya tomadas.

---

## REGISTRO DE ENTRADAS

---

### ENTRADA 001 — Inicio del sistema de memoria
**Fecha**: Sesión inicial
**Tipo**: Inicialización

Se inició el sistema de memoria del proyecto **Maestro Bíblico PWA**.

**Contexto de inicio:**
- El proyecto parte de un prompt de sistema teológico extenso (Maestro Bíblico) con identidad, fundamento teológico, método hermenéutico, método exegético, criterios pedagógicos, formato de respuesta y límites doctrinales completamente definidos.
- El usuario solicita convertir este sistema en una PWA instalable en celular y computadora.
- Se crearon los archivos `CLAUDE.md` y `MEMORIA.md` como infraestructura de contexto persistente.
- Stack elegido: HTML5 + CSS3 + JavaScript vanilla — decisión basada en simplicidad de deploy y máxima compatibilidad.
- Deploy target: Vercel.
- API: Anthropic `/v1/messages` con `claude-sonnet-4-20250514`.

**Estado inicial del proyecto**: Archivos de contexto creados. PWA en construcción.

---

### ENTRADA 002 — Construcción inicial de la PWA
**Fecha**: Sesión inicial
**Tipo**: Decisión técnica + implementación

**Decisiones tomadas:**
- Diseño de la UI: sobrio, elegante, de tonos oscuros — coherente con el peso teológico del proyecto. Se eligió paleta oscura (azul-gris profundo) con tipografía serif para encabezados (evocando textos clásicos y académicos) y sans-serif limpia para el cuerpo de conversación.
- El historial de conversación se mantiene en memoria de sesión (array `messages`) y se envía completo en cada llamada API.
- El system prompt completo del Maestro Bíblico se inyecta como `system` en cada request.
- Service Worker implementado con estrategia cache-first para assets estáticos.
- `manifest.json` configurado con `display: standalone` para comportamiento de app nativa.
- La API key se gestiona mediante variable de entorno de Vercel (`ANTHROPIC_API_KEY`) — nunca hardcodeada en el frontend.
- Se implementó un endpoint proxy en Vercel (`/api/chat`) para proteger la API key.

**Archivos creados en esta sesión:**
- `CLAUDE.md`
- `MEMORIA.md`
- `index.html` (app principal)
- `manifest.json`
- `sw.js` (service worker)
- `api/chat.js` (endpoint proxy Vercel)
- `vercel.json` (configuración de deploy)
- Íconos SVG generados inline (sin dependencia de archivos externos de imagen)

---

## PLANTILLA PARA FUTURAS ENTRADAS

```
### ENTRADA XXX — [Título descriptivo]
**Fecha**: [Sesión/fecha]
**Tipo**: [corrección doctrinal / ajuste pedagógico / preferencia del usuario / error corregido / mejora aplicada / patrón exitoso / cambio de criterio / problema recurrente / nueva regla]

[Descripción del aprendizaje, corrección o decisión]

**Impacto en el proyecto**: [qué cambió y por qué]
**Referencia**: [CLAUDE.md sección X si aplica]
```

---

## ERRORES A EVITAR (acumulativo)

*(Se irán agregando con el tiempo)*

- No hardcodear la API key en ningún archivo del frontend
- No simplificar el system prompt del Maestro Bíblico
- No usar diseño lúdico o colorido que contradiga el tono teológico del proyecto

---

## PATRONES EXITOSOS (acumulativo)

*(Se irán agregando con el tiempo)*

- Inyección del system prompt completo en cada llamada API: garantiza coherencia doctrinal en toda la sesión
- Proxy API en Vercel Functions: protege la clave y permite CORS correcto

---

## PREFERENCIAS DEL USUARIO (acumulativo)

- Idioma: español rioplatense (argentino) — uso de "vos", "vosotros" → preferir "ustedes" en contexto bíblico
- Tono: serio, profundo, sin excesos de entusiasmo superficial
- Stack: preferencia por simplicidad técnica sobre complejidad innecesaria

---

## PROBLEMAS RECURRENTES (acumulativo)

*(Se irán registrando)*

---

## NUEVAS REGLAS SURGIDAS DURANTE EL TRABAJO (acumulativo)

*(Se irán registrando)*
