# 🤖 Ingeniería de Prompting y Agentes Autónomos

Cuadernos de Google Colab del AVE **Ingeniería de Prompting y Agentes Autónomos** · Pregrado · Facultad de Ingeniería · **Universidad Ean**.

A lo largo del curso construirás a **Nexo**, el asistente de IA de la **Cooperativa Raíces**. Nexo empieza como un chatbot que a veces inventa respuestas y termina como un sistema de agentes que usa herramientas, consulta documentos, trabaja en equipo y es supervisado con trazas, métricas y alertas.

---

## 📚 Contenido

| Módulo | Cuaderno | Temas | Abrir |
|:---:|---|---|:---:|
| **1** | **C1 · Nexo aprende a hablar** | Fundamentos de los LLM, temperatura y muestreo, tokens y ventana de contexto, embeddings, anatomía del prompt (rol, contexto, instrucción, formato y ejemplos) | [![Abrir en Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/github/ProfeCamilaSilva/Ingenier-a-de-Prompting-y-Agentes-Aut-nomos/blob/main/M1_C1_Nexo_aprende_a_hablar.ipynb) |
| **1** | **C2 · Nexo aprende a pensar** | *Zero-shot* y *few-shot*, *chain-of-thought*, *system prompts* y plantillas, salidas estructuradas (JSON con Pydantic), *prompt patterns*, evaluación de exactitud, consistencia y alucinaciones | [![Abrir en Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/github/ProfeCamilaSilva/Ingenier-a-de-Prompting-y-Agentes-Aut-nomos/blob/main/M1_C2_Nexo_aprende_a_pensar.ipynb) |
| **2** | **C1 · Nexo actúa: herramientas y ReAct** | Chatbot vs. agente, *function calling*, bucle ReAct (razonar → actuar → observar), planificación de metas de varios pasos | [![Abrir en Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/github/ProfeCamilaSilva/Ingenier-a-de-Prompting-y-Agentes-Aut-nomos/blob/main/M2_C1_Nexo_actua_herramientas_y_ReAct.ipynb) |
| **2** | **C2 · Nexo recuerda: RAG, memoria y guardrails** | RAG desde cero (fragmentar, embeddings, indexar, recuperar), respuestas con fuente y "no sé", métrica de recuperación, memoria de corto y largo plazo, MCP, *guardrails* de entrada, salida y acción | [![Abrir en Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/github/ProfeCamilaSilva/Ingenier-a-de-Prompting-y-Agentes-Aut-nomos/blob/main/M2_C2_Nexo_recuerda_RAG_memoria_guardrails.ipynb) |
| **3** | **C1 · El equipo de Nexo: multiagente** | Cuándo usar varios agentes, clase `Agente` reutilizable, patrones enrutador, secuencial (redactor → revisor) y orquestador-trabajadores, *human-in-the-loop* y escalamiento | [![Abrir en Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/github/ProfeCamilaSilva/Ingenier-a-de-Prompting-y-Agentes-Aut-nomos/blob/main/M3_C1_El_equipo_de_Nexo_multiagente.ipynb) |
| **3** | **C2 · Supervisar a Nexo: trazas, métricas y alertas** | Trazabilidad de decisiones, métricas de eficacia y seguridad con línea base, tablero de control, alertas, plan de delegación progresiva y esquema de supervisión, preparación del proyecto final | [![Abrir en Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/github/ProfeCamilaSilva/Ingenier-a-de-Prompting-y-Agentes-Aut-nomos/blob/main/M3_C2_Supervisar_a_Nexo_trazas_metricas_alertas.ipynb) |

> Los cuadernos están pensados para trabajarse **en orden**: cada uno retoma lo que Nexo aprendió en el anterior.

---

## 🚀 Cómo empezar

1. **Abre el cuaderno** con el botón *Abrir en Colab* de la tabla.
2. **Guarda tu propia copia**: en Colab, *Archivo → Guardar una copia en Drive*. Así tus cambios no se pierden.
3. **Consigue una API key de Gemini** (gratuita) en [Google AI Studio](https://aistudio.google.com/apikey).
4. **Guárdala como secreto de Colab**:
   - En la barra izquierda de Colab, haz clic en el ícono de la llave 🔑 (*Secretos*).
   - Crea un secreto llamado exactamente `GOOGLE_API_KEY` y pega tu clave.
   - Activa *Acceso del cuaderno*.
5. **Ejecuta las celdas en orden**, de arriba hacia abajo. La primera celda instala las librerías necesarias.

> ⚠️ **Nunca pegues tu API key directamente en el código** ni la compartas en tus entregas. Usa siempre los secretos de Colab.

---

## 🧰 Requisitos técnicos

- Una cuenta de Google (para Colab y AI Studio).
- No necesitas instalar nada en tu computador: todo corre en Google Colab.
- Librerías que instala cada cuaderno: [`google-genai`](https://pypi.org/project/google-genai/) y [`pydantic`](https://pypi.org/project/pydantic/).
- Modelos: familia **Gemini Flash** a través de la API de Google.

---

## 🛠️ Problemas frecuentes

| Problema | Qué hacer |
|---|---|
| `SecretNotFoundError` o error de autenticación | Revisa que el secreto se llame `GOOGLE_API_KEY` y que el acceso del cuaderno esté activado. |
| Error `429` / *quota exceeded* | Alcanzaste el límite del plan gratuito. Espera uno o dos minutos y vuelve a ejecutar la celda. |
| `NameError` (una variable "no existe") | Te saltaste una celda. Ve a *Entorno de ejecución → Ejecutar anteriores*. |
| El cuaderno se desconectó | Vuelve a ejecutar desde la primera celda: Colab borra la memoria al reiniciar. |
| Las respuestas del modelo cambian entre ejecuciones | Es normal: los LLM no son deterministas. El Cuaderno 1 explica por qué. |

---

## 👩‍🏫 Autoría

Material elaborado por **Camila Silva Gómez** para el AVE *Ingeniería de Prompting y Agentes Autónomos* de la Universidad Ean.

La Cooperativa Raíces, Nexo y los personajes de los casos son ficticios y se usan con fines educativos.
