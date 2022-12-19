# Métodos abstractos
---
#JavaScript #Clases #Métodos #
## Ideas clave
---
### Convertir métodos a métodos abstractos 
## Notas
---
Un método abstracto es un método que no ejecuta nada y muestra un error al 
tratar de llamarlo
```JavaScript
retirarDeCuenta(cantidad) {
      throw new Error('Debe implementar el metodo en su clase')
  }
```
Este método puede servir para indicar al desarrollador que cree un método 
especializado en cada clase
## Resumen
---
Los métodos abstractos no realizan ninguna acción y se protegen al tratar de 
ejecutarlos
Los métodos abstractos deben ser sobrescritos por las clases hijas.