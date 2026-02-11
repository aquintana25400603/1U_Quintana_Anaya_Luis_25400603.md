# Principios SOLID

## 2.1. S - Single Responsibility Principle (SRP)

Definición: "Una clase debe tener una sola razón para cambiar". Esto significa que cada clase debe encargarse de una única funcionalidad o parte del problema.
Ejemplo: En lugar de tener una clase Factura que calcule el total, lo guarde en la base de datos y además genere un PDF, deberías tener tres: Factura (datos), FacturaRepositorio (guardar) y FacturaImpresora (PDF).
¿Por qué es importante? Reduce el acoplamiento. Si necesitas cambiar cómo se guarda en la base de datos, no corres el riesgo de romper accidentalmente la lógica de impresión.

## 2.2. O - Open/Closed Principle (OCP)
Definición: "Las entidades de software (clases, módulos, funciones) deben estar abiertas para la extensión, pero cerradas para la modificación".
¿Por qué es importante? Te permite añadir nuevas funcionalidades sin tocar el código que ya funciona y ha sido testeado. Se logra comúnmente mediante el uso de interfaces o herencia.

## 2.3. L - Liskov Substitution Principle (LSP)
Definición: "Si S es un subtipo de T, los objetos de tipo T pueden ser reemplazados por objetos de tipo S sin alterar las propiedades del programa".
¿Por qué es importante? Asegura que la herencia sea correcta. Un ejemplo clásico de error es hacer que Avestruz herede de Ave si el método Volar() está en Ave; el código fallará porque el avestruz no vuela.

## 2.4. I - Interface Segregation Principle (ISP)
Definición: "Ningún cliente debe ser forzado a depender de métodos que no utiliza". Es mejor tener muchas interfaces específicas que una sola interfaz general "gorda".
¿Por qué es importante? Evita que las clases implementen métodos "vacíos" o lancen excepciones de "no implementado" solo para cumplir con una interfaz demasiado grande.
  
## 2.5. D - Dependency Inversion Principle (DIP)
Definición: "Las dependencias deben estar en las abstracciones, no en las concreciones". Los módulos de alto nivel no deben depender de los de bajo nivel; ambos deben depender de interfaces.
¿Por qué es importante? 
Hace que tu código sea flexible. Si tu aplicación depende de una interfaz BaseDeDatos, puedes cambiar de MySQL a MongoDB sin cambiar ni una línea de tu lógica de negocio principal.

