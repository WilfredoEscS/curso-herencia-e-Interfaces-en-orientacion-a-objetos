# Análisis de código repetido
---
#JavaScript #Clases #Atributos
## Ideas clave
---
### Desventajas del código duplicado | Definición rápida de atributos públicos
## Notas
---
Los atributos públicos pueden definirse automáticamente en el `constructor`
```JavaScript
export class Cuenta {
  /* Atributosd de clase */
  #cliente;
  #saldo;
  static cantidaDeCuentas = 0;

constructor(agencia, cliente, numero, saldo) {
    this.agencia = agencia;
    this.cliente = cliente;
    this.numero = numero;
    this.#saldo = saldo;
    Cuenta.cantidaDeCuentas++;
  }
```

Si dos clases son muy parecidas, e incluso tienen los mismos métodos hay que hacer un sola clase que realize  las funciones de ambas 

Con lo que tendríamos lo siguiente
```JavaScript
const cuentaDeJuan = new Cuenta("001", cliente, "1");
const cuentaAhorroDeJuan = new Cuenta("001", cliente, "3");
```
En lugar de esto
```JavaScript 
const cuentaDeJuan = new CuentaCorriente("001", cliente, "1");
const cuentaAhorroDeJuan = new CuentaAhorro("001", cliente, "3");
```

Al tener código duplicado, el mantenerlo se vuelve el doble de trabajo, por eso es mejor evitarlo
## Resumen
---
Los atributos públicos pueden definirse en el constructor
Declarar atributos privados, previene que los datos puedan corromperse a causa de un error
El código duplicado genera mas trabajo de mantenimiento