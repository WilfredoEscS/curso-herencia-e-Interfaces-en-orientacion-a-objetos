# Métodos privados y protegidos
---
#Métodos #JavaScript #Clases #Sobreescritura #Atributos 
## Ideas clave
---
### Sobreescritura de métodos con atributos privados | Métodos privados
## Notas
---
Al intentar sobrescribir  completamente un método con atributos privados de la clase padre
```JavaScript
export class CuentaCorriente extends Cuenta {
  retirarDeCuenta(cantidad) {
    valor = valor * 1.05
    if (cantidad < this.#saldo)
      this.#saldo -= cantidad;
    return this.verSaldo();
  }
// #saldo es un atributo privado de la clase padre 'Cuenta'
```
Resultara un error
```Shell
SyntaxError: Private field '#saldo' must be declared in an enclosing class
```
En lugar de eso hay que sobrescribir el método, modificar lo que deseemos, y luego llamar al método del padre pasando los parámetros modificados
```JavaScript
export class CuentaCorriente extends Cuenta {
  retirarDeCuenta(cantidad) {
    cantidad = cantidad * 1.05;
    super.retirarDeCuenta(cantidad);
  }
}
```
O pasar valores distintos de un parámetro por cada clase
```JavaScript
//Metodo de Clase `Cuenta`
  retirarDeCuenta(cantidad,comision) {
    cantidad = cantidad * (1 + comision/100)
    if (cantidad < this.#saldo)
      this.#saldo -= cantidad;
    return this.verSaldo();
  }
```
```JavaScript
//Método de clase 'CuentaCorriente'
retirarDeCuenta(cantidad) {
    super.retirarDeCuenta(cantidad, 5);
  }
```
```JavaScript
//Método de clase 'CuentaAhorro'
retirarDeCuenta(cantidad) {
    super.retirarDeCuenta(cantidad, 2);
  }
```
Un método privado en se define con el símbolo `__`, aunque no presente restricción sirve como indicativo de que es privado 
```JavaScript
_retirarDeCuenta(cantidad,comision) {
    cantidad = cantidad * (1 + comision/100)
    if (cantidad < this.#saldo)
      this.#saldo -= cantidad;
    return this.verSaldo();
```
[Información adicional](https://ljcl79.medium.com/herencia-en-programaci%C3%B3n-orientada-a-objetos-370cf3f97402)
## Resumen
---
Para sobrescribir parcialmente métodos con atributos privados debemos llamar al método padre desde el método hijo y pasar parámetros modificados o nuevos
Los métodos privados en JavaScript no tienen restricción, solo es indicativo