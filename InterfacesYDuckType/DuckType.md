# Duck Type
---
#JavaScript #DuckType
## Ideas clave
---
### Tipado dinámico 
## Notas
---
En el Duck Typing solo son relevantes los aspectos del objeto a utilizar, no 
el tipo de objeto en cuestión

Si un objeto sobre el que se llama la función login cumple los requisitos 
para ser autenticado
```JavaScript
static login(usuario, clave) {
// Verifica si el objeto contiene la interfaz y si ésta es una función 
    if ("autenticable" in usuario && usuario.autenticable instanceof Function)
      return usuario.autenticable(clave);
    else return false;
  }
```
Significa que el objeto es un usuario autenticable
## Resumen
---
Es un método de tipado, aplicado a lenguajes de tipado dinámico
Permite omitir la declaración del tipo de objeto, a cambio de una 
comprensión clara de los aspectos que lo definen, una buena documentación, y pruebas para asegurar su correcto uso y funcionamiento 