# Acceso y sobreescritura de clase padre 
---
#JavaScript #Clases #Superclases #Herencia #Métodos #Sobreescritura 
## Ideas clave
---
### Acceso a clase padre con `super` | Sobrescribiendo superclase
## Notas
---
Todas las subclases pueden llamar a los métodos pertenecientes a la clase padre
```JavaScript
//Declaración de metodo en la clase padre
export class Cuenta {
  prueba(){
      console.log("Metodo padre")
    }
```
```JavaScript
}//Extension de la subclase
export class CuentaCorriente extends Cuenta {
}
```
```JavaScript
//Llamado del metodo desde la subclase
cuentaDeJuan.prueba();
// Devuelve 'Metodo padre' en la consola
```
Incluso desde otros métodos de las subclases utilizando la palabra `super`
```JavaScript
export class CuentaCorriente extends Cuenta {
  prueba() {
    super.prueba();
    console.log("Metodo hijo")  }
}
/*
Devuelve 
'Metodo padre'
'Metodo hijo'en la consola 
*/
```
Tambien es posible sobrescribir el método.
```JavaScript
export class CuentaCorriente extends Cuenta {
  prueba() {
    console.log("Metodo hijo")  
    }
}
//Devuelve solamente 'Metodo hijo'en la consola 
```
## Resumen
---
Las subclases pueden acceder a los métodos de su superclase
Si un método tiene el mismo nombre en la clase padre y la clase hijo, al llamarla desde la clase hijo, esta predominara y se ejecutara solo el método hijo
Eso permite sobrescribir métodos por clases especificas o hacer combinaciones llamando al método padre dentro del método hijo