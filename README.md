# 🌱 Horticultura Expert Assistant - Sistema RAG para Horticultura

**Combina un chatbot especializado con búsqueda semántica en documentos técnicos**  
*Usando OpenAI GPT-3.5, Sentence Transformers y FAISS*

---

## 📌 Descripción

Este proyecto implementa un asistente de horticultura inteligente que:
1. **Procesa documentos técnicos** (PDFs) para extraer conocimiento estructurado.
2. **Combina un modelo LLM** (GPT-3.5-turbo) con **búsqueda semántica** (RAG) para respuestas precisas.
3. Opera en dos fases claramente separadas:
   - **Preprocesamiento**: Extracción y vectorización de contenido.
   - **Chatbot**: Interacción conversacional aumentada con contexto.

---

## 🛠️ Estructura del Repositorio
```
horticultura-expert/
├── RAG_preprocessing.ipynb # Notebook de procesamiento de PDFs
├── Horticulture_Assistant.ipynb # Notebook del chatbot interactivo
├── data/
│ ├── Principles_of_Horticulture.pdf # Ejemplo de documento técnico
│ ├── horticultura_chunks.npy # Fragmentos de texto procesados
│ ├── horticultura_embeddings.npy # Embeddings de los fragmentos
│ └── horticultura_index.faiss # Índice de búsqueda semántica
├── requirements.txt # Dependencias
└── README.md # Este archivo
```

---

## 🔧 Instalación

1. **Clona el repositorio**:
   ```bash
   git clone https://github.com/tu-usuario/horticultura-expert.git
   cd horticultura-expert

2. Instala dependencias:
bash
pip install -r requirements.txt

3. Prepara tus documentos:
Coloca tus PDFs en la carpeta data/.
Edita RAG_preprocessing.ipynb para apuntar a tu archivo.

## 🚀 Uso

1. **Procesamiento de Documentos**

Ejecuta `RAG_preprocessing.ipynb` para:

Extraer texto de PDFs.
Generar embeddings con `all-MiniLM-L6-v2`.
Crear un índice FAISS para búsqueda rápida.
Salidas:
✅ horticultura_chunks.npy
✅ horticultura_embeddings.npy
✅ horticultura_index.faiss

2. **Chatbot de Horticultura**

Ejecuta Horticulture_Assistant.ipynb para:

Cargar los embeddings preprocesados.
Iniciar un chatbot que combina:
- Conocimiento del LLM (GPT-3.5-turbo).
- Contexto de los documentos (búsqueda semántica).

## 🌟 Características Clave

- **Separación clara** entre preprocesamiento y aplicación.
- **Optimización para CPU/GPU**: Usa FAISS para búsqueda eficiente.
- **Prompt engineering**: Combina contexto documental con instrucciones al LLM.
- **Extensible**: Fácil adaptación a otros dominios (medicina, derecho, etc.).

## 📝 Notas Técnicas

- **Modelos Embedding**: `all-MiniLM-L6-v2` (384 dimensiones, balance precisión-velocidad).
- **Librerías clave**:
  - `PyPDF2`: Extracción de texto.
  - `sentence-transformers`: Generación de embeddings.
  - `faiss`: Búsqueda semántica.
  - `openai`: Integración con GPT-3.5.
