## Errores y modificaciones:
1- la etiqueta input type="text", linea 31 se modifico agregandole "required" para que el dato sea requerido para su funcion, adicional, se le colocó una longitud maxima de 3 caracteres ya que el 100 contiene 3 caracteres y es el numero maximo y una funcion onKeypress, en donde, solo acepte numeros en su campo del cero (0) al nueve (9). Ya que es uno de los requerimientos, solo aceptar numeros

2- la etiqueta input type="submit", linea 32 se modifico, agregandole un id y desactivando el boton, y se activa hasta que se ingrese un dato en la caja de texto 

3- linea 44, se modifico la variable randomNumber, dejandola de la siguiente forma: let randomNumber =Math.floor(Math.random()*100)+1. Se agrego +1 debido a que la funcion Math.floor redondea hacia abajo el un numero entero mas cercano. 

4- linea 46, se modifico el valor de const ATTEMPS a 10, estaba en 5.

5- linea 49, se modifico el valor de la clase lowOrHi dentro de document.querySelector, agregandole el punto "." para definirla como clase.

6- linea 59, se agrego una sentencia if, que detalla una condicion en donde, si se ingresa un numero diferente al entero(decimal), arrojará un alert("Valido solo números enteros").

7- linea 64, se corrigió la sentencia if(userGuess===randomNumber), ya que tenía como resultado perdiste, siendo lo correcto: lastResult.textContent = 'Felicitaciones! adivinaste el número!';
      lastResult.style.backgroundColor = 'green';.

8- linea 69, se corrigió la sentencia else if(guessCount === ATTEMPS), ya que tenía como resultado 'Felicitaciones! adivinaste el número!', siendo lo correcto:
lastResult.textContent = '!!!Pérdistes!!!';
      lastResult.style.backgroundColor = 'red';

9- linea 74, se corrigió la sentencia else, ya que el lastResult.style.backgroundColor = 'green' siendo lo correcto: lastResult.style.backgroundColor = 'black'

10- linea 76, se corrigió la sentencia if(userGuess < randomNumber) {
        lowOrHi.textContent = 'El número es mayor!';
      } else if(userGuess > randomNumber) {
        lowOrHi.textContent = 'El número es menor!';
      } ya que estaba erronea, segun los requerimientos, es asi: if(userGuess < randomNumber) {
        lowOrHi.textContent = 'El número es menor!';
      } else if(userGuess > randomNumber) {
        lowOrHi.textContent = 'El número es mayor!';
      }

11- linea 87, se corrigió la linea de codigo guessSubmit.addeventListener('click', checkGuess). siendo la correcta: guessSubmit.addEventListener('click', checkGuess). Event, es con inicial mayuscula.

12- linea 95, se corrigio la linea de codigo resetButton.addeventListener('click', resetGame). siendo la correcta: resetButton.addEventListener('click', resetGame). Event, es con inicial mayuscula. 

13- linea 114, se corrigio la linea de codigo randomNumber = Math.floor(Math.random()) + 1. siendo la correcta: randomNumber = Math.floor(Math.random()*100) + 1. Agregando el valor 100 a multiplicarse con Math.random(); esto para que pueda arrojar un numero entre 1 y 100.

14- se creó la funcion habilitar(). sirve para bloquear el boton "Ingresar el numero aleatorio", al momento que se ingresa al juego, y se desbloquea, cuando detecta que existe un caracter en la caja de texto  "guessField".