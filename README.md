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

