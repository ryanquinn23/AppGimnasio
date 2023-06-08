## API

Aplicacion

## BASE DE DATOS 💻

## TABLAS

- users:

id
name
email
password
avatar
role
createdAt
modifiedAt

- exercises:

id
name
description
photo
typologyId
muscleGroupId
userId
createdAt
modifiedAt

- likes:

id
userId
exerciseId
createdAt

- favourites:

id
userId
exerciseId
createdAt

- typology:
  id
  exerciseId
  description
  createdAt

- muscleGroup:
  id
  exerciseId
  description
  createdAt

## ENDPOINTS 🏁

## Users Endpoints:

- POST ['/users'] ▶️ Registro de usuario pendiente de validar ◾ newUser.✅
- PUT - ['/users/validate/:regCode'] ▶️ Valida a un usuario recién registrado. >>opcional:brevo.com<<
- POST - ['/users/login'] ▶️ Logea a un usuario retornando un token. loginUser.✅
- GET - ['/users/:userId'] ▶️ Retorna información de un usuario(mi propio usuario)✅
- GET - ['/users'] ▶️ Retorna información de un usuario del token(mi propio usuario)✅

## Exercises:

## Usuario Admin

- POST ['/exercises'] ▶️ Registro de un nuevo ejercicio/entrenamiento Token ✅
- GET ['/exercises/:exerciseId']▶️ Devuelve info de un ejercicio en concreto Token ✅
- PUT ['/exercises/:exerciseId'] ▶️ Modificar ejercicio. Token ✅
- DELETE ['/exercises/:exerciseId'] ▶️ Eliminar ejercicio. Token ✅

## Usuario normal

- POST ['/exercises/:exerciseId/likes'] Dar like ✅
- DELETE ['/exercises/:exerciseId/likes'] Eliminar like ✅
- GET ['/exercises'] ▶️ Listado de todos los ejercicios con filtros. Token hace falta estar logeado para ver ejercicios ✅
- POST ['/exercises/:exerciseId/favorites/:userid'] Anade un ejercicio a la lista favoritos **JUEV/VIERNES**
- DELETE ['/exercises/:exerciseId/favorites/:userId'] Eliminar un ejercicio a la lista favoritos jueves **JUEV/VIERNES**

Si nos da tiempo:

# bonus track

- PUT - ['/users/password'] - Resetea la contraseña de un usuario. Token
- PUT - ['/users/avatar'] - Permite actualizar el avatar del usuario. ➡️ Token
- PUT - ['/users/validate/:regCode'] ▶️ Valida a un usuario recién registrado. >>opcional:brevo.com'anonimo'<<
- PUT - ['/users/password/recover'] - Envía al usuario un correo de recuperación de contraseña. >regis
- DELETE - ['/users/:userId] - Eliminar a un usuario - el admin
