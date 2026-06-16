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

## Resultado de chunking + embedding

================================================================================
ESTRATEGIA: small
Numero de chunks: 48
Longitud minima: 22
Longitud maxima: 500
Longitud media: 353.02
Ejemplo de chunk 1:
TENERIFE – LUGARES DE INTERÉS
SITIOS QUE VER
ZONA NORTE
• Santa Cruz de Tenerife:
Santa Cruz de Tenerife es la capital de la isla. Quizás la ruta a seguir si vais a Santa
Cruz sería:

- Aparcar en el aparcamiento del Parque Marítimo (ubicación).
- Caminar por la Avenida Marítima hasta Plaza de España (ubicación).
- Por el camino de la Avenida Marítima, ver el auditorio de Tenerife (ubicación).
- Una vez llegados a Plaza España, callejear un poco (subir la Calle Castillo
  Metadata: {'producer': 'PyPDF', 'creator': 'Microsoft Word', 'creationdate': '2025-07-13T20:00:01+00:00', 'title': 'Microsoft Word - TENERIFE.docx', 'moddate': '2025-07-13T20:00:01+00:00', 'source': 'c:\\Repositorios\\practicaLLMs\\TENERIFE.pdf', 'total_pages': 25, 'page': 0, 'page_label': '1', 'source_name': 'TENERIFE.pdf', 'start_index': 0, 'chunk_id': 0, 'chunk_size': 500, 'chunk_overlap': 80, 'strategy_name': 'small'}

Ejemplo de chunk 2:

- Una vez llegados a Plaza España, callejear un poco (subir la Calle Castillo
  dirección Plaza Weyler - ubicación –; ir hacia el Parque García Sanabria -
  ubicación -; y bajar de nuevo hacia Plaza de España pasando por la Plaza del
  Príncipe - ubicación).
- Volver de nuevo a por el coche.
- Ir hacia la playa de Las Teresitas (ubicación).
  Los puntos de interés sugeridos son estos:
  o Parque Marítimo César Manrique [vídeo - ubicación]
  Conjunto de piscinas naturales.
  Metadata: {'producer': 'PyPDF', 'creator': 'Microsoft Word', 'creationdate': '2025-07-13T20:00:01+00:00', 'title': 'Microsoft Word - TENERIFE.docx', 'moddate': '2025-07-13T20:00:01+00:00', 'source': 'c:\\Repositorios\\practicaLLMs\\TENERIFE.pdf', 'total_pages': 25, 'page': 0, 'page_label': '1', 'source_name': 'TENERIFE.pdf', 'start_index': 396, 'chunk_id': 1, 'chunk_size': 500, 'chunk_overlap': 80, 'strategy_name': 'small'}
  ================================================================================
  ESTRATEGIA: medium
  Numero de chunks: 31
  Longitud minima: 81
  Longitud maxima: 900
  Longitud media: 533.06
  Ejemplo de chunk 1:
  TENERIFE – LUGARES DE INTERÉS
  SITIOS QUE VER
  ZONA NORTE
  • Santa Cruz de Tenerife:
  Santa Cruz de Tenerife es la capital de la isla. Quizás la ruta a seguir si vais a Santa
  Cruz sería:
- Aparcar en el aparcamiento del Parque Marítimo (ubicación).
- Caminar por la Avenida Marítima hasta Plaza de España (ubicación).
- Por el camino de la Avenida Marítima, ver el auditorio de Tenerife (ubicación).
- Una vez llegados a Plaza España, callejear un poco (subir la Calle Castillo
  dirección Plaza Weyler - ubicación –; ir hacia el Parque García Sanabria -
  ubicación -; y bajar de nuevo hacia Plaza de España pasando por la Plaza del
  Príncipe - ubicación).
- Volver de nuevo a por el coche.
- Ir hacia la pla
  Metadata: {'producer': 'PyPDF', 'creator': 'Microsoft Word', 'creationdate': '2025-07-13T20:00:01+00:00', 'title': 'Microsoft Word - TENERIFE.docx', 'moddate': '2025-07-13T20:00:01+00:00', 'source': 'c:\\Repositorios\\practicaLLMs\\TENERIFE.pdf', 'total_pages': 25, 'page': 0, 'page_label': '1', 'source_name': 'TENERIFE.pdf', 'start_index': 0, 'chunk_id': 0, 'chunk_size': 900, 'chunk_overlap': 150, 'strategy_name': 'medium'}

Ejemplo de chunk 2:
o Auditorio de Tenerife [vídeo - ubicación]
o Plaza de España [vídeo - ubicación]
Metadata: {'producer': 'PyPDF', 'creator': 'Microsoft Word', 'creationdate': '2025-07-13T20:00:01+00:00', 'title': 'Microsoft Word - TENERIFE.docx', 'moddate': '2025-07-13T20:00:01+00:00', 'source': 'c:\\Repositorios\\practicaLLMs\\TENERIFE.pdf', 'total_pages': 25, 'page': 1, 'page_label': '2', 'source_name': 'TENERIFE.pdf', 'start_index': 0, 'chunk_id': 1, 'chunk_size': 900, 'chunk_overlap': 150, 'strategy_name': 'medium'}
================================================================================
ESTRATEGIA: large
Numero de chunks: 28
Longitud minima: 81
Longitud maxima: 1174
Longitud media: 582.82
Ejemplo de chunk 1:
TENERIFE – LUGARES DE INTERÉS
SITIOS QUE VER
ZONA NORTE
• Santa Cruz de Tenerife:
Santa Cruz de Tenerife es la capital de la isla. Quizás la ruta a seguir si vais a Santa
Cruz sería:

- Aparcar en el aparcamiento del Parque Marítimo (ubicación).
- Caminar por la Avenida Marítima hasta Plaza de España (ubicación).
- Por el camino de la Avenida Marítima, ver el auditorio de Tenerife (ubicación).
- Una vez llegados a Plaza España, callejear un poco (subir la Calle Castillo
  dirección Plaza Weyler - ubicación –; ir hacia el Parque García Sanabria -
  ubicación -; y bajar de nuevo hacia Plaza de España pasando por la Plaza del
  Príncipe - ubicación).
- Volver de nuevo a por el coche.
- Ir hacia la pla
  Metadata: {'producer': 'PyPDF', 'creator': 'Microsoft Word', 'creationdate': '2025-07-13T20:00:01+00:00', 'title': 'Microsoft Word - TENERIFE.docx', 'moddate': '2025-07-13T20:00:01+00:00', 'source': 'c:\\Repositorios\\practicaLLMs\\TENERIFE.pdf', 'total_pages': 25, 'page': 0, 'page_label': '1', 'source_name': 'TENERIFE.pdf', 'start_index': 0, 'chunk_id': 0, 'chunk_size': 1200, 'chunk_overlap': 150, 'strategy_name': 'large'}

Ejemplo de chunk 2:
o Auditorio de Tenerife [vídeo - ubicación]
o Plaza de España [vídeo - ubicación]
Metadata: {'producer': 'PyPDF', 'creator': 'Microsoft Word', 'creationdate': '2025-07-13T20:00:01+00:00', 'title': 'Microsoft Word - TENERIFE.docx', 'moddate': '2025-07-13T20:00:01+00:00', 'source': 'c:\\Repositorios\\practicaLLMs\\TENERIFE.pdf', 'total_pages': 25, 'page': 1, 'page_label': '2', 'source_name': 'TENERIFE.pdf', 'start_index': 0, 'chunk_id': 1, 'chunk_size': 1200, 'chunk_overlap': 150, 'strategy_name': 'large'}

## Resultado retrieval

Pregunta: Cual es una visita imprescindible en Tenerife para un primer viaje?
Estrategia: medium
k: 4
Latencia retrieval (ms): 395.94
Latencia generacion (ms): 4170.68
Token usage: {'input_tokens': 937, 'output_tokens': 174, 'total_tokens': 1111, 'input_token_details': {'audio': 0, 'cache_read': 0}, 'output_token_details': {'audio': 0, 'reasoning': 0}}

Una visita imprescindible en Tenerife para un primer viaje es el Parque Nacional del Teide. Subir al Teide es considerado esencial para conocer la isla. Se recomienda subir por la carretera TF24 desde La Laguna, haciendo una parada en el Mirador de La Tarta para disfrutar de un espectacular mar de nubes si el clima lo permite. Al llegar al Parador de las Cañadas del Teide, se puede aparcar y visitar el mirador de La Ruleta, desde donde se obtiene una de las vistas más famosas de Tenerife. Además, es posible subir al pico del Teide utilizando los teleféricos y visitar el Centro de Visitantes de El Portillo, que es gratuito. Para los amantes de la astronomía, subir de noche al Teide es una experiencia única para observar uno de los cielos estrellados más impresionantes del mundo.

Fuentes:

- TENERIFE.pdf | pagina 14 | chunk 17
- TENERIFE.pdf | pagina 0 | chunk 0
- TENERIFE.pdf | pagina 10 | chunk 11
- TENERIFE.pdf | pagina 15 | chunk 18

## TESTS

### Test "small"

================================================================================
EVALUACION retrieval | estrategia=small | k=3

---

Casos evaluados: 2
Retrieval OK: 2 / 2
Top 1 OK: 2 / 2
Respuestas con fuentes: 2 / 2
Latencia media retrieval (ms): 444.52
Latencia media generacion (ms): 3527.64
================================================================================
EVALUACION retrieval | estrategia=small | k=5

---

Casos evaluados: 2
Retrieval OK: 2 / 2
Top 1 OK: 2 / 2
Respuestas con fuentes: 2 / 2
Latencia media retrieval (ms): 596.0
Latencia media generacion (ms): 4536.81

### Test "medium"

================================================================================
EVALUACION retrieval | estrategia=medium | k=3

---

Casos evaluados: 2
Retrieval OK: 2 / 2
Top 1 OK: 2 / 2
Respuestas con fuentes: 2 / 2
Latencia media retrieval (ms): 242.14
Latencia media generacion (ms): 4710.68
================================================================================
EVALUACION retrieval | estrategia=medium | k=5

---

Casos evaluados: 2
Retrieval OK: 2 / 2
Top 1 OK: 2 / 2
Respuestas con fuentes: 2 / 2
Latencia media retrieval (ms): 275.82
Latencia media generacion (ms): 3530.11

## Test "large"

================================================================================
EVALUACION retrieval | estrategia=large | k=3

---

RESUMEN
Casos evaluados: 2
Retrieval OK: 2 / 2
Top 1 OK: 2 / 2
Respuestas con fuentes: 2 / 2
Latencia media retrieval (ms): 221.33
Latencia media generacion (ms): 3540.49
================================================================================
EVALUACION retrieval | estrategia=large | k=5

---

Casos evaluados: 2
Retrieval OK: 2 / 2
Top 1 OK: 2 / 2
Respuestas con fuentes: 2 / 2
Latencia media retrieval (ms): 255.82
Latencia media generacion (ms): 3863.37
