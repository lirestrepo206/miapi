# Documentación API Users

Este api permite una administración básica de usuarios que se almacenan en memoria usando la tecnológia de Python y Flask
 
## subtitulo

### Metodos soportados

- **GET**
- **POST**

### Ruta principal del API

- **/v1/users**


### GET


- **endpoint**: /v1/users
- **Http Codes Response:**

    -200 OK
    500 internal server error

### GET

>Este metodo te entrega todos los usuarios que estan en memoria

- **Json Schema Response:**
```json
{
  "$schema": "http://json-schema.org/draft-07/schema#",
  "title": "Generated schema for Root",
  "type": "array",
  "items": {
    "type": "object",
    "properties": {
      "age": {
        "type": "number"
      },
      "name": {
        "type": "string"
      }
    },
    "required": [
      "age",
      "name"
    ]
  }
}
```

- **Example Response:**
```json

[
	{
		"age": 31,
		"name": "Liliana"
	}
]
```

### POST

>Este metodo inserta un usuario en el modelo de negocio

- **endpoint**: /v1/users
- **Http Codes Response:**

    - 201 Created
    - 400 
        - empty body
        - bad data type
        incomplete body
    - 500 internal server error

- **Json Schema Body:**
```json
{
  "$schema": "http://json-schema.org/draft-07/schema#",
  "title": "schema body API",
  "type": "object",
  "properties": {
    "name": {
      "type": "string"
    },
    "age": {
      "type": "number"
    }
  },
  "required": [
    "name",
    "age"
  ]
}
```
- **Example Body:**
```json

{
 "name":"Liliana",
 "age":31

}
```
