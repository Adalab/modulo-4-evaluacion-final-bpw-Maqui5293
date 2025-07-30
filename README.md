📘 Documentación básica de la API – Los Simpson Quotes API

Esta API permite gestionar frases míticas de Los Simpson, conectándolas con los personajes y los capítulos donde fueron dichas.

✅ Base URL

http://localhost:4000

📌 Endpoints disponibles

🔹 GET /frases

Lista todas las frases, incluyendo el personaje que la dijo y el título del capítulo.

📅 Ejemplo de respuesta:

[
{
"id": 1,
"texto": "D'oh!",
"marca_tiempo": "00:05",
"descripcion": "Frase icónica de Homer",
"personaje": "Homer",
"capitulo": "Homer el Grande"
}
]

🔹 GET /frases/:id

Devuelve los detalles de una frase específica por su ID.

🔹 POST /frases

Crea una nueva frase.

📄 Body JSON:

{
"texto": "¡Ay, caramba!",
"marca_tiempo": "00:10",
"descripcion": "Frase típica de Bart",
"personaje_id": 2,
"capitulo_id": 1
}

🔹 PUT /frases/:id

Actualiza una frase existente por su ID.

📄 Body JSON igual que POST.

🔹 DELETE /frases/:id

Elimina una frase por su ID.

🛠️ Requisitos técnicos

Backend con Node.js + Express

Base de datos MySQL

Variables de entorno gestionadas con dotenv

📦 Instalación

Clona el repositorio:

git clone <URL>

Instala dependencias:

npm install

Configura tu .env:

DB_HOST=localhost
DB_USER=root
DB_PASS=
DB_NAME=simpsons
PORT=4000

Inicia el servidor:

npm run dev

🗂️ Estructura recomendada
├── index.js
├── schema.sql
├── .env
├── .gitignore
├── package.json
├── README.md
