# Herencia en JavaScript
---
#JavaScript #Clases #Herencia #Superclases #Subclases 
## Ideas clave
---
### ¿Que es herencia en JavaScript? | Características de superclases  y subclases| Extender clases
## Notas
---
La herencia en JavaScript implica que una clase herede todas las funcionalidades de otra al definirse como **subclase** de la misma

la palabra reservada `extends` crea una subclase a partir de cualquier clase personalizada 
```JavaScript
export class CuentaCorriente extends Cuenta {
  static cantidaDeCuentas = 0;
  constructor() {
    CuentaCorriente.cantidaDeCuentas++;
  }
}
```
La subclase hereda todas las funcionalidades de la "superclase" a partir de la que fue creada

Para que la subclase pueda acceder a las funcionalidades de las superclase hay que llamarla utilizando la palabra reservada `super`
```JavaScript
export class CuentaCorriente extends Cuenta {
  static cantidaDeCuentas = 0;
//Primero le pasa los parametros al constructor y este se la pasa al la superclase
  constructor(agencia, cliente, numero,) {
    super(agencia, cliente, numero, 0);
    CuentaCorriente.cantidaDeCuentas++;
  }
}
```

La palabra clave `super` también puede utilizarse para llamar otras funciones del objeto padre.
## Resumen
---
La forma correcta de extender las clases es mediante la herencia
La Herencia pone las funcionalidades de la superclase a disposición de  las subclases
Para esto se hace uso de la palabra clave `super`
