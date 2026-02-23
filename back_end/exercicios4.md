1. ABS: Este método tem a função de retornar o valor absoluto de um número, isto significa 
que o retorno será sempre positivo. Caso seja informado um valor negativo à este método., ele retornará 
o mesmo como positivo. Por exemplo, caso utilizemos o valor -1234, ele será convertido para 1234.
Essa operação é chamada também de módulo, e pode ser calculada matematicamente como a raiz quadrada do valor elevado ao quadrado.

<html>
<head>
<title>...</title>
</head>

<body>
  <script>
    var valor1 = Math.abs (-1234);
    alert (valor1);
  </script>
</body>
</html>


2. ACOS: Este método retornará o arco cosseno (em radianos) de um número. 

<html>
<head>
<title>...</title>
</head>

<body>
  <script>
    var valor1 = Math.acos (0.14);
    alert (valor1);
  </script>
</body>
</html>


3. ASIN: Este método retorna o arco seno (em radianos) de um valor.
   
<html>
<head>
<title>...</title>
</head>

<body>
  <script>
    var valor1 = Math.asin (0.14);
    alert (valor1);
  </script>
</body>
</html>


4. CEIL: Este método retorna um inteiro maior ou igual a um número. O resultado deste método é equivalente ao arredondamento
de um número. A lógica do arredondamento de um número é que se um número é um valor  positivo como 14,6
 o resultado do arredondamento será 15, quando o número for um valor negativo,
como-14,6 o resultado é -14 Vejamos isso em um exemplo pratico.

<html>
<head>
<title>...</title>
</head>

<body>
  <script>
    var valor1 = Math.ceil (14.6);
    alert (valor1);
  </script>
</body>
</html>


5. <html>
<head>
<title>...</title>
</head>

<body>
  <script>
    var valor1 = Math.ceil (-14.6);
    alert (valor1);
  </script>
</body>
</html>


6. COS: Este método retornará o cosseno (em radianos) de um número.
   
 <html>
<head>
<title>...</title>
</head>

<body>
  <script>
    var valor1 = Math.cos (0.14);
    alert (valor1);
  </script>
</body>
</html>

7.EXP: Este método retornará o valor da constante de Euler elevada ao número informado, ou seja, E elevado ao parâmetro.

<html>
<head>
<title>...</title>
</head>

<body>
  <script>
    var valor1 = Math.exp (0.0007);
    alert (valor1);
  </script>
</body>
</html>

8.FLOOR: Este método retorna o maior inteiro menor ou igual a um número.

<html>
<head>
<title>...</title>
</head>

<body>
  <script>
    var valor1 = Math.floor (100.25);
    var valor2 = Math.floor (-100.25);
    alert (valor1);LOG: Este método retorna o logaritmo natural de um número (base E).
    alert (valor2);
  </script>
</body>
</html>

9.LOG: Este método retorna o logaritmo natural de um número (base E).

<html>
<head>
<title>...</title>
</head>

<body>https://www.onlinegdb.com/#editor_1
  <script>
    var valor1 = Math.log (2.2);
    alert (valor1);
  </script>
</body>
</html>

10.MAX: Este método retorna o maior valor entre dois números.

<html>
<head>
<title>...</title>
</head>

<body>
  <script>
    var valor1 = Math.max ( 3,9);
    alert (valor1);
  </script>
</body>
</html>

11.MIN: Este método retorna o menor valor entre dois números.

<html>
<head>
<title>...</title>
</head>

<body>
  <script>
    var valor1 = Math.min ( 3,9);
    alert (valor1);
  </script>
</body>
</html>

12.POW (base, expoente): Este método retorna a base elevada à potência do expoente. Por exemplo, 2 elevado a décima potência é 1024.

<html>
<head>
<title>...</title>
</head>

<body>
  <script>
    var valor1 = Math.pow ( 1024,2);
    alert (valor1);
  </script>
</body>
</html>

13.RANDOM: Este método retorna um número aleatório entre 0 e 1 com até 15 dígitos. Este número aleatório é definido através do relógio do computador.

<html>
<head>
<title>...</title>
</head>

<body>
  <script>
    alert (Math.random ());
  </script>
</body>
</html>

14. ROUND: Com este método é possível arredondar um valor. O arredondamento segue a regra de arredondamento que vimos anteriormente.

<html>
<head>
<title>...</title>
</head>

<body>
  <script>
    var valor1 = Math.round (121.6);
    alert (valor1);
  </script>
</body>
</html>

15.SIN: Este método retorna o seno de um número.

<html>
<head>
<title>...</title>
</head>

<body>
  <script>
    var valor1 = Math.sin (1.4);
    alert (valor1);
  </script>
</body>
</html>


16.SQRT: Retorna a raiz quadrada de um número.

<html>
<head>
<title>...</title>
</head>

<body>
  <script>
    var valor1 = Math.sqrt (9);
    alert (valor1);
  </script>
</body>
</html>

17.TAN: Retorna a tangente de um número, que é equivalente a divisão do seno pelo cosseno deste mesmo valor.

<html>
<head>
<title>...</title>
</head>

<body>
  <script>
    var valor1 = Math.tan (1.5);
    alert (valor1);
  </script>
</body>
</html>








