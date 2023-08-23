# Budget-app

![Static Badge](https://img.shields.io/badge/node_version-18.16.1-44cc44)
![Static Badge](https://img.shields.io/badge/npm_version-9.8.0-4444cc)
![Static Badge](https://img.shields.io/badge/nest_version-10.1.9-cc4444)
![Static Badge](https://img.shields.io/badge/state-development-cc1111)

## Objetivo

El objetivo principal de esta aplicación es proporcionar a los usuarios una manera sencilla pero eficiente de controlar sus gastos mensuales y fomentar el ahorro responsable de su dinero. Sabemos lo importante que es mantener un registro claro de los gastos realizados, y esta aplicación está diseñada para facilitar esa tarea.

## Instalacion

Para poder desplegar el backend primero se necesita crear un contenedor con [docker](https://www.docker.com/) que contenga la base de datos en [postgres](https://www.postgresql.org/). Luego se debe crear un archivo .env en el que se debe agregar la variable de entorno `DATABASE_URL`.

```
$ docker run -d -p 5432:5432 -e POSTGRES_USER=user -e POSTGRES_PASSWORD=example -e POSTGRES_DB=budget-app postgres
```
Para ejecutar la aplicacion se debe hacer de la siguiente manera:

```
$ git clone url
$ cd budget-backend
$ npm install
$ npx prisma generate
$ npx prisma migrate dev
$ npm run start
```
## Anotaciones

Para desplegar la aplicacion tambien se puede usar docker compose o docker swarm, pero de momentos estos no estan implementados ya que la app aun esta en desarrollo.