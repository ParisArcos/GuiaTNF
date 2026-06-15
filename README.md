# Entorno para `GuiaTNF`

Este directorio contiene todo lo necesario para ejecutar el entregable de la
asignatura de LLMs.

El notebook principal es:

```text
guia_tnf.ipynb
```

## API key

El notebook usa la API de OpenAI.

Crea un archivo `.env` a partir del ejemplo:

```bash
cp .env.example .env
```

Rellena:

```text
OPENAI_API_KEY="..."
```

Puedes cambiar los modelos con:

```text
OPENAI_GENERATION_MODEL="gpt-4.1-mini"
OPENAI_FAST_MODEL="gpt-4.1-mini"
OPENAI_EMBEDDING_MODEL="text-embedding-3-small"
```

## Windows

En Windows nativo puedes usar Python `3.11` y `requirements.txt`.
Instala tambien Graphviz y asegurate de que `dot` este disponible en el `PATH`.

Desde esta carpeta:

```powershell
py -3.11 -m venv .venv
.\.venv\Scripts\activate
python -m pip install --upgrade pip
pip install -r requirements.txt
python -m ipykernel install --user --name guia-tnf --display-name "Python (guia-tnf)"
jupyter lab guia_tnf.ipynb
```

## Dependencias principales

- `openai`
- `openai-agents`
- `mcp`
- `python-dotenv`
- `pydantic`
- `pandas`
- `graphviz`
- `tiktoken`
- `jupyterlab`
- `ipykernel`
