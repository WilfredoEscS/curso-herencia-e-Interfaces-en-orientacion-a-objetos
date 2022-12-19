# Propiedad constructor
---
#JavaScript #Propiedades #Clases #Herencia
## Ideas clave
---
### Evitar creación de objetos de una clase | Propiedad constructor
## Notas
---
Una clase abstracta es una que solo se debe extender, no deben crearse 
instancias de ella sino de sus clases hijo

En el concepto de herencia de objetos el constructor pasa de la subclase a la 
superclase.

La propiedad `constructor` retorna una referencia a la función del Object que 
creó el objeto de la instancia
```JavaScript
const cuentaSimple = new Cuenta("001", cliente, "098", 250);
console.log(cuentaSimple.constructor);
```
Devuelve
```PowerShell
# node .\index.js
[class Cuenta]
```
## Resumen
---
Las clases abstractas son aquellas que solo deben ser extendidas, no 
instanciadas
Al crear un instancia de las subclases se ejecuta el constructor de la superclase 
padre
La palabra clase constructor retorna una referencia a la clase cuyo constructor 
inicializo la instancia 