# NVIDIA DLI — Building RAG Agents with LLMs

This repository contains Jupyter notebooks and datasets aligned with the NVIDIA’s Deep Learning Institute “Building RAG Agents with LLMs” course. 

https://learn.nvidia.com/courses/course-detail?course_id=course-v1:DLI+S-FX-15+V1 

The course is intended for hands-on practice with retrieval-augmented generation: ingesting documents, embedding/indexing, retrieving relevant context, and composing grounded answers.

## Repository Layout
- `chatbot/` — example chatbot, tools and frontend pieces used in the labs
- `composer/` — microservice and composer examples, Docker compose config
- `context/` — example context and supporting text used by notebooks
- `docker_router/` — router utility and Dockerfile for routing examples
- `frontend/` — frontend/demo server and related files
- `imgs/` — images used by slides and notebooks
- `llm_client/` — client/server LLM example code and Dockerfiles
- `slides/` — presentation slides for the course
- `solutions/` — solution notebooks and example answers
- `*.ipynb` Multiple Notebook files for each section
- `README.md` — this file

## Quick Start
1. Clone the repo:  
   `git clone https://github.com/your-org/building-rag-agents-llms.git && cd building-rag-agents-llms`
2. Create the environment:  
   - Conda: `conda env create -f environment.yml && conda activate rag-agents`
   - Pip: `python -m venv .venv && source .venv/bin/activate && pip install -r requirements.txt`
3. Launch Jupyter:  
   `jupyter lab` (or `jupyter notebook`)

## Configuration (optional)
Create a `.env` file for API keys and local settings used by certain notebooks:

```
OPENAI_API_KEY=your_key
OLLAMA_HOST=http://localhost:11434 
EMBEDDING_MODEL=text-embedding-3-large
INDEX_DIR=.indexes
```

Adjust variables per your tooling (OpenAI/Ollama/other providers). Each notebook notes its required settings.

## Data
Place your documents (PDF/MD/HTML/text) in `data/`. Notebooks expect relative paths (e.g., `data/knowledge_base/`). If you change paths, update the corresponding cells.

## Notes
- GPU acceleration is optional but recommended when using larger models.
- Some notebooks may offer interchangeable backends (e.g., FAISS vs. in-memory) to simplify setup.

## License
Unless otherwise stated, code in this repository is provided under the MIT License.

## Acknowledgments
Inspired by NVIDIA’s “Building RAG Agents with LLMs” workshop materials.