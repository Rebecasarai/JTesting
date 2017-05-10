# JUnit Testing and Testing Suite

![Imagen](http://www.swtestacademy.com/wp-content/uploads/2015/11/Junit_Logo.png)

Debemos de realizar una clase Math, muy simple, de addicion. A este le creamos un Test para testear las posibles soluciones.

Creamos la clase Math.java, la cual compilamos, teniendo por supuesto los jars necesarios en la dirección elegida. La mia es: /home/alumnado-pc21/misjars/spring-framework-4.3.7.RELEASE/libs/*:..

# Cómo hacerlo funcionar

## Testing
  - Git clone:
```sh
$ git clone https://github.com/Rebecasarai/JTesting.git
$ cd JTesting
```

  - Compilamos primeramente la clase Math.java dando la dirección de los jars, recordando la dependencia:
```sh
$ javac -cp /home/alumnado-pc21/misjars/spring-framework-4.3.7.RELEASE/libs/*:.  Math.java
```
  - Compilamos el testing:
```sh
$ javac -cp /home/alumnado-pc21/misjars/spring-framework-4.3.7.RELEASE/libs/*:.  MathTest.java
```
- Corremos el test:
```sh
$ java -cp /home/alumnado-pc21/misjars/spring-framework-4.3.7.RELEASE/libs/*:. org.junit.runner.JUnitCore  MathTest
```

Deberia de resultar en:
```sh
$ java -cp /home/alumnado-pc21/misjars/spring-framework-4.3.7.RELEASE/libs/*:. org.junit.runner.JUnitCore  MathTest

JUnit version 4.12
....
Time: 0,004

OK (4 tests)
```

## Testing Suite
- Ya hemos creado un est Suite, el cual nos permite automatizar dos clases de Test: 
    
> @Suite.SuiteClasses({
>    MathTestSolucion.class,
>    TestPerson.class
> })
  - Compilamos, y realizamos el test: 
```sh
$ javac -cp /home/alumnado-pc21/misjars/spring-framework-4.3.7.RELEASE/libs/*:.  MathJunitTestSuite.java

$ java -cp /home/alumnado-pc21/misjars/spring-framework-4.3.7.RELEASE/libs/*:. org.junit.runner.JUnitCore  MathJunitTestSuite
JUnit version 4.12
.....
Time: 0,005

OK (5 tests)
