# Interfaces 
---
#JavaScript #Polimorfismo #Variables #Clases #Interfaz
## Ideas clave
---
### Autenticación de objetos | Definición de una interfaz | Encapsulamiento de interfaz
## Notas
---
Un atributo o método existente en dos clases sirve como interfaz para
comunicarlas
El atributo clave presente en la clase Empleado
```JavaScript
export class Empleado {
  #clave;
  #nombre;
  #dui;
  #salario;
}
```
Y también en la clase Cliente
```JavaScript
export class Cliente {
  #clave;
  duiCliente;
  nombreCliente;
  rutCliente;
}
```
Sirven como interfaz para que SistemaAutenticacion acceda a ellas
Pasando el valor como un parámetro 
```JavaScript
export class SistemaAutenticacion {
  static login(usuario, clave) {
    return usuario.clave == clave;
  }
}
```
Aunque funciona de esta manera, es mejor encapsular la interfaz en un 
método.
```JavaScript
export class Empleado {

autenticable(clave) {
    return clave == this.#clave;
  }
}
```
Y acceder al atributo mediante éste en  lugar de usar un getter
```JavaScript
export class SistemaAutenticacion {

static login(usuario, clave) {
    return usuario.autenticable(clave)
  }
}
```
Es posible tener diferentes implementaciones en cada clase, modificando la interface
```JavaScript
export class Empleado {
//Retorna falso, bloqueando la autenticacion de los clientes
autenticable(clave) {
    return false
  }
}
```

## Resumen
---
Es mas seguro implementar interfaces a traves de métodos en lugar de
atributos
El polimorfismo permite tener diferentes implementaciones en cada clase, 
lo que se logra modificando la interfaz
