# Verificando propiedades y tipos
---
#JavaScript #Propiedades #TiposDeDatos #Polimorfismo
## Ideas clave
---
### Verificación de presencia interfaz | Verificación tipo de interfaz 
## Notas
---
##### Operador in
`in` devuelve true si la propiedad especificada esta en el objeto especificado 
o su prototipo
```JavaScript
if ("autenticable" in usuario)
  return usuario.autenticable(clave);
else return false;
```
##### InstanceOF
InstanceOf puede verificar si un elemento es una función a través de la palabra 
reservada `Function` (Con inicial mayúscula)
```JavaScript
if ("autenticable" in usuario && usuario.autenticable instanceof Function)
  return usuario.autenticable(clave);
else return false;
```
## Resumen
---
Para evitar que un error en la interpretación del tipo de interfaz ocurra hay que
validarlo
Para ello contamos con los operadores `in` e `instanceOf`
