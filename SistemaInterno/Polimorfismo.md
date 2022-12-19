# Polimorfismo
---
#JavaScript #Clases #Polimorfismo #Métodos 

## Ideas clave
---
### Polimorfismo en programación | Funciones estáticas | Gestion de clases con getters y setters
## Notas
---
##### El polimorfismo
Es la capacidad que nos proporciona un lenguaje de programación
orientado a objetos para tratar un objeto como si fuera un objeto de otra 
clase.

Identificar una función como estática es igual que con los atributos 
estáticos
```JavaScript
export class SistemaAutenticacion {

  static login(empleado, clave) {
    return empleado.clave == clave;
  }
}
```
Si no se declara un getter con la palabra reservada `get` es reconocida como 
función
```JavaScript
 get clave() {
    return this.#clave;
  }
//Retorna el valor de '#clave' para esta instancia

clave() {
    return this.#clave;
  }
//Informa que 'clave' es una funcion: [Function: clave]
```
## Resumen
---
El polimorfismo permite llamar métodos o atributos con el mismo nombre, 
que son de clases no heredables
Las funciones estáticas se declaran igual que los atributos estáticos
Es importante diferenciar getters y setters de los demás métodos