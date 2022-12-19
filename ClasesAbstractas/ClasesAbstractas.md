# Protegiendo clase abstracta
---
#JavaScript #Clases #Herencia #Propiedades
## Ideas clave
---
### Protegiendo clase | Definición de clase abstracta
## Notas
---
La instruction
```JavaScript
throw new Error("Mensaje")
```
devuelve un error definido por el usuario y cancela la ejecución de la función actual
Utilizándolo es posible proteger una clase abstracta para que no sea instanciada
```JavaScript
 constructor( agencia, cliente, numero, saldo) {
    if (this.constructor == Cuenta){
      throw new Error('No se deben crear instancias de la clase Cuenta')
    }
```
Validando la clase de la instancia con la propiedad constructor, y devuelve
```PowerShell
Error: No se deben crear instancias de la clase Cuenta
```
[Mas información](https://ljcl79.medium.com/las-clases-abstractas-qu%C3%A9-son-y-para-qu%C3%A9-sirven-8328b92db680)
## Resumen
---
Solamente devolver un mensaje de error no es suficiente para proteger una 
clase abstracta
Con ayuda de un `throw` es posible envirar el mensaje y frenar la inicialización 
de la instancia
Utilizar clases generales para crear instancias eventualmente puede dificultar 
diferenciarlas , además de otros inconvenientes