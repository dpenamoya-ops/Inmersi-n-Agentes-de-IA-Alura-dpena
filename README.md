# 🤖 Agente Inteligente RAG + Web con LangGraph

Este proyecto implementa un agente inteligente capaz de responder preguntas utilizando:

- 📄 Documentos locales (PDFs) mediante RAG
- 🌐 Información en tiempo real desde la web

El sistema decide automáticamente qué fuente utilizar.

---

## 🚀 Características

- Carga y procesamiento de PDFs
- Búsqueda semántica con FAISS
- Integración con modelos Gemini (Google)
- Agente con toma de decisiones automática
- Respuestas formateadas en Markdown
- Orquestación con LangGraph

---

## 🧠 Arquitectura
            ┌─── RAG ───→ Documentos PDF ───┐
            Usuario → Agente → Markdown → Respuesta
            └─── Web ───→ Búsqueda online ──┘

---

## 🛠️ Tecnologías utilizadas

- Python
- LangChain
- LangGraph
- FAISS
- Google Generative AI (Gemini)
- SerpAPI

---

## 📦 Instalación

```bash
pip install google-genai
pip install langchain-community pypdf
pip install langchain-text-splitters
pip install langchain-google-genai faiss-cpu
pip install langgraph google-search-results markdown fpdf2

🔑 Configuración
Debes configurar tus API Keys:
GEMINI_API_KEY = "tu_api_key"
SERPAPI_API_KEY = "tu_api_key"

📂 Uso

1. Cargar PDFs
Sube tus documentos a la carpeta PDFs/.

2. Ejecutar el agente
ejecutar_agente("¿Tu pregunta aquí?")

El usuario hace una pregunta

El agente decide:

RAG (documentos internos)

Web (internet)

Se obtiene contexto relevante

Se genera una respuesta en Markdown

📌 Ejemplos
Pregunta interna (RAG)

¿Dónde se mantuvo concentrado el mix de productos?

Pregunta externa (Web)

¿Cuántos mundiales tiene Brasil?

⚠️ Limitaciones

Dependencia de APIs externas (Gemini, SerpAPI)

Calidad depende de los documentos cargados

Clasificación RAG/Web puede fallar en casos ambiguos

🔮 Mejoras futuras

Mejor clasificación con modelo entrenado

UI (Streamlit o web app)

Cache de consultas

Evaluación de respuestas

Multi-documento avanzado

👨‍💻 Autor

Proyecto desarrollado por David Peña como parte del curso de Inmersión DEV AGENTES DE AI (Alura).
