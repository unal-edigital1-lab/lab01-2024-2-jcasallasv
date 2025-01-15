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


Y por ultimo con el comando always hacemos que siempre se ejecute lo que está dentro, que en este caso es sumar las entradas y asignarlo en la salida.

La principal diferencia entre modulo sum1bcc y modulo sum1bcc_primitive es que, a pesar de que ambas describen un sumador de 2 bits por sus entradas y salidas, en la primera se está realizando la ejecución de la suma, en la segunda solamente se describe el diseño de su circuito lógico



### sumador 
