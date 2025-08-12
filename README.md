# pruebas-Qunit 
## **Proyecto: Pruebas de JavaScript con QUnit**

```
Este proyecto es una práctica sencilla de pruebas automatizadas usando **QUnit**, una librería de JavaScript para testear funciones.
```

## ⚙️ Requisitos

```
No necesitas instalar nada. Solo un navegador moderno como:

- Chrome
- Firefox
- Edge
- Safari
```

## 🧠 ¿Qué hace este proyecto?

```
Contiene una función llamada `multiplicar(a, b)` y un conjunto de pruebas automáticas que verifican si la función funciona correctamente.

Usamos QUnit para comprobar:

- Si los resultados son los esperados
- Si el código sigue funcionando después de cambios
- Qué pasa si usamos tipos de datos no esperados (por ejemplo, strings)
```


## **Ejemplo de código mal:**

```
function multiplicar(a, b) {
return a + b; | ¡Esto está mal!
}
///

// si sale en verde es porque está bien
// si sale en rojo es porque está mal
```

## 📁 Archivos del proyecto

```
## 📄 test.html explicado
Este archivo es el que se va a probar.
```

## Archivo de pruebas
```
**FUNCIÓN A PROBAR**
    function multiplicar(a, b) {
      return a * b;
    }
```
## PRUEBAS CON QUNIT
```
    QUnit.module('Pruebas de función multiplicar', function() {
      QUnit.test('2 * 3 debe ser 6', function(assert) {
        assert.equal(multiplicar(2, 3), 6, '2 * 3 = 6');
      });
        
      QUnit.test('0 * 10 debe ser 0', function(assert) {
        assert.equal(multiplicar(0, 10), 0, '0 * 10 = 0');
      });

      QUnit.test('-5 * 2 debe ser -10', function(assert) {
        assert.equal(multiplicar(-5, 2), -10, '-5 * 2 = -10');
      });

      QUnit.test('Multiplicar por string no numérico debe dar NaN', function(assert) {
        assert.ok(isNaN(multiplicar(4, "hola")), '4 * "hola" = NaN');
      });
    });
```




