# lab01- sumador 
## Julián Camilo Casallas

## Informe de laboratorio 
Se debe analizar lo que está en el códígo de module sum1bcc_primitive.
En el argumento se tienen las entradas y salidas del sumador (A, B, Ci,Cout,S)

Cuando se registra las entradas se usa este códígo: 

```verilog
  input  A;
  input  B;
  input  Ci;***
```

Sin embargo el compilador no lo puede procesar debido a que una linea tiene unos caracteres que no debería estar después del punto y coma (***).

Con el código de sum1bcc se tiene el tipo de sumador que queremos, en donde nuestras entradas (A, B, Ci) producen las salidas (S, Cout)

Con la linea 

```verilog
reg [1:0] st;
```

Se genera el registro del sumador de dos bits

Después se hace la asignación al resultado del sumador:

```verilog
assign S = st[0];
assign Cout = st[1];
```

Donde S está definido con el bit menos significativo y Cout con el más significativo








### sumador 
