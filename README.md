# IMPORTANTE: PROFE TUVE UN PROBLEMA CON KALI, NO ME ESTA DEJANDO CASI QUE NI ENTRAR, ESTOY SOLUCIONANDO ESO LO MAS RAPIDO POSIBLE PARA PODER PONER LOS FORMATOS .PY Y .G4 DE LA MANERA QUE ES, DE MOMENTO TUVE QUE PONERLOS EN UN TXT

# ANTLR

# Características 

Soporta:

Operaciones aritméticas, Factorial y Funciones matemáticas como lo son: sin(x), cos(x), tan(x), raíz cuadrada, logaritmo natural, logaritmo base 10 y cambio entre grados y radianes (deg()  activa modo grados) y (rad() → activa modo radianes)

Estructura del proyecto:

```
ANTLR4/
│── labeldExpr.g4           # Gramática ANTLR
│── Calc.java               # Main en Java
│── EvalVisitor.java        # Visitante en Java
│── calc.py                 # Main en Python
│── EvalVisitor.py          # Visitante en Python
```

Ejecución en Java
Generar archivos con ANTLR:
```
antlr4 -visitor labeldExpr.g4
javac *.java
```

Ejecutar:
```
java -cp .:antlr-4.13.1-complete.jar Calc

```
Ejecución en Python
Generar archivos con ANTLR:
```
antlr4 -Dlanguage=Python3 -visitor labeldExpr.g4
```

Ejecutar:
```
python3 calc.py
```
Ejemplos de uso
```
deg()
sin(30)       → 0.5
cos(60)       → 0.5
rad()
sin(3.1416/2) → 1.0
sqrt(25)      → 5.0
log(1000)     → 3.0
ln(2.71828)   → 1.0
5!            → 120
2^8           → 256.0
