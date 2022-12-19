# Identificando por tipo de clase
---
#JavaScript #Clases
## Ideas clave
---
### Diferenciar instancias de la misma clase utilizando atributos | Especializacion de clases
## Notas
---
Si una sola clase maneja varios tipos de instancias es necesario diferenciaros.

Una alternativa e pasar un atributo `tipo` al constructor de la clase
```JavaScript
constructor(agencia, cliente, numero, saldo, tipo) {
    this.agencia = agencia;
    this.cliente = cliente;
    this.numero = numero;
    this.#saldo = saldo;
    this.tipo = tipo;
    }
```
Y pasarle el valor al crear las instancias
```JavaScript
const cuentaDeJuan = new Cuenta("001", cliente, "1", 0, "Corriente");
const cuentaAhorroDeJuan = new Cuenta("001", cliente, "3", 0, "Ahorro");
```
Pero si se ingresa un valor invalido en el atributo
```JavaScript
//'Ahorros' en lugar de 'Ahorro'
const cuentaAhorroDeJuan = new Cuenta("001", cliente, "3", 0, "Ahorros");
```
Necesitaríamos tomar otras medidas para validarlo, lo que no es eficiente

Para solventar esto existe la herencias de clases
## Resumen
---
Para diferenciar una instancia de otra de la misma clase podemos usar un atributo tipo, y validarlo para asignar características distintas a cada tipo de instancia
Pero esto puede no ser del todo efectivo, por eso JavaScript ofrece alternativas para este mismo propósito 