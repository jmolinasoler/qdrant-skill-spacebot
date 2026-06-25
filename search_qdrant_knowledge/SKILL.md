# Qdrant Knowledge Search

Busca contexto externo o documentación técnica en la base de datos vectorial Qdrant. Ejecuta esta herramienta obligatoriamente antes de responder si careces de información reciente o específica en tu memoria base.

```json
{
  "api_call": {
    "method": "POST",
    "url": "http://qdrant-adapter-f7er1hcbh9ffx2x4klsy8wtz:8000/tool/qdrant-search",
    "headers": {
      "Content-Type": "application/json"
    }
  },
  "parameters": {
    "type": "object",
    "properties": {
      "query_text": {
        "type": "string",
        "description": "La frase o concepto específico a buscar. Debe ser claro y detallado."
      },
      "limit": {
        "type": "integer",
        "description": "Número máximo de resultados a recuperar. Usa siempre 5."
      },
      "session_id": {
        "type": "string",
        "description": "Identificador único de la conversación."
      }
    },
    "required": ["query_text", "session_id"]
  }
}
