# Iniciamos el proyecto
npm init -y

# Instalamos los paquetes: express, pg y cors
npm i express pg cors

# Lanzamos servidor
node index.js

# Instalamos paquete nodemon modo desarrollo
npm i nodemon -D

# Lanzamos servidor con nodemon
nodemon index.js

:::::::::::::::::::::::::::::::::::::
| DATA BASE                         |
:::::::::::::::::::::::::::::::::::::
# Conección a la base de datos
psql -U postgres

# Listar bases de datos
\l

# Creamos una base de datos
CREATE DATABASE perntodo;

# Nos conectamos a la base de datos
\c perntodo

# Ver tablas
\dt

# Creamos una tabla
CREATE TABLE todo (
  id SERIAL PRIMARY KEY,
  description VARCHAR(255) NOT NULL
);

# Hacemos una consulta
SELECT * FROM todo;

# Eliminar columna
ALTER TABLE todo 
DROP COLUMN created_at;

# Añadir una columna
ALTER TABLE todo
ADD COLUMN description VARCHAR(255) NOT NULL;

:::::::::::::::::::::::::::::::::::::
| CLIENT - REACT                    |
:::::::::::::::::::::::::::::::::::::

# Creamos el proyecto
npx create-react-app client