# llm_avm_95298
Repositorio de ollama para sistemas inteligentes 

## 1 Instalación de Ollama

Para instalar ollama accedemos a la página de [Ollama] (https://ollama.com/download/linux), en una terminal se ejecuta el siguiente comando 

````bash
$ curl -fsSL https://ollama.com/install.sh | sh
````

## 2 Ejecutar el servidor 

Una vez instalando se ejecuta el servidor ollama con el siguiente comando 

````bash
$ ollama serve
````

## 3 Descargar algún modelo 
En la página de [modelo](https://ollama.com/library) de ollama se busca el modelo deseado y se descarga con el siguiente comando:

````bash
$ ollama pull tinyllama
````
## 4 Prueba de request a la API REST

````bash
curl -X POST http://localhost:11434/api/generate -d '{
  "model": "tinyllama",
  "prompt": "Why is the sky blue?"
}'
````

## 5 Realizar un request  a stream

````bash
$ curl -X POST http://localhost:11434/api/generate -d '{
  "model": "tinyllama",
  "prompt": "Why is the sky blue?"
  "stream" : false
}'
````

## 6 Realizar un request a groq 

````bash
curl "https://api.groq.com/openai/v1/chat/completions" \
  -X POST \
  -H "Content-Type: application/json" \
  -H "Authorization: Bearer ${GROQ_API_KEY}" \
  -d '{
         "messages": [
           {
             "role": "user",
             "content": "¿Por qué el cielo es azul?"
           }
         ],
         "model": "gemma-7b-it",
         "stream": false
       }'
````
  


