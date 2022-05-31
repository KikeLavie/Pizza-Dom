Instrucciones
Solo trabajaremos con el js/index.jsarchivo. Como verá, el archivo contiene algo de código. El archivo está diseñado para tener una separación de preocupaciones y hacer que el código sea escalable. Esta arquitectura es muy parecida a la que usará con React.

En esta arquitectura, hay una variable statecon diferentes valores, como pepperoniinicialmente establecida en true. Cuando el usuario haga clic en él, el valor cambiará al contrario (ejemplo: false).

En esta arquitectura, también hay una función renderEverythingque representa la pizza, los botones y el precio según el estado. Esta función debe ejecutarse cada vez que se cambia el estado, porque se debe cambiar la pizza, los botones y el precio. Para dar un ejemplo, cuando state.pepperonies true, la función:

hacer visible el pepperoni en la pizza,
agregue una clase activeal botón "pepperoni",
actualizar el panel de precios.

Iteración 1: agregar y eliminar coberturas
Hay cinco botones a la izquierda del generador de pizza. Tres de ellos tienen que agregar o quitar ingredientes de la pizza. Escriba el JavaScript necesario para esos tres botones para agregar y quitar pepperoni, champiñones y pimientos verdes de la pizza. No te preocupes por actualizar el precio . Lo haremos más tarde.

Cada topping individual tiene su propio elemento HTML.

<!-- When this button is clicked -->
<button class="btn btn-pepperoni active">Pepperoni</button>

<!-- ... -->

<!-- Hide/show all the following sections at the same time -->
<section class="pep one">1</section>
<section class="pep two">2</section>
<!-- ... -->
<!-- When this button is clicked -->
<button class="btn btn-mushrooms active">Mushrooms</button>

<!-- ... -->

<!-- Hide/show all the following sections at the same time -->
<section class="mushroom one">
  <div class="cap">1</div>
  <div class="stem"></div>
</section>
<section class="mushroom two">
  <div class="cap">2</div>
  <div class="stem"></div>
</section>
<!-- ... -->
<!-- When this button is clicked -->
<button class="btn btn-green-peppers active">Green peppers</button>

<!-- ... -->

<!-- Hide/show all the following sections at the same time -->
<section class="green-pepper one"></section>
<section class="green-pepper two"></section>
<!-- ... -->
Cree el código para ocultar/mostrar esos elementos cuando se hace clic en los botones. Para ello, tendrás que:

Agregue un detector de eventos de clic en <button class="btn btn-mushrooms">y <button class="btn btn-green-peppers">(pepperoni ya está hecho)
Escriba el código de las funciones renderMushrooms()yrenderGreenPeppers()

Iteración 2: opciones de salsa y corteza
En esta iteración, su objetivo es:

Agregue un detector de eventos de clic <button class="btn btn-sauce">y cambiestate.whiteSauce
Escribe la funciónrenderWhiteSauce()
Agregue un detector de eventos de clic <button class="btn btn-crust">y cambiestate.glutenFreeCrust
Escribe la funciónrenderGlutenFreeCrust()
Como puede ver, el valor inicial de state.whiteSaucey state.glutenFreeCrustes falso. El motivo es que, por defecto, queremos una pizza con pepperoni, champiñones, pimientos verdes pero sin salsa blanca ni masa sin gluten.

Por ahora, no te preocupes por actualizar el precio .

<!-- Example of a pizza with white-sauce and a gluten-free crust -->
<section class="crust crust-gluten-free">
  <section class="cheese"></section>
  <section class="sauce sauce-white"></section>
</section>

<!-- Example of a pizza with no white-sauce and no gluten-free crust -->
<section class="crust">
  <section class="cheese"></section>
  <section class="sauce"></section>
</section>

Iteración 3: hacer que los botones estén activos o no
Actualmente, todos los botones tienen el mismo aspecto, sin importar si la opción está activada o no. Si te fijas, todos los botones tienen una activeclase.

<button class="btn btn-pepperoni active">Pepperoni</button>
Escriba la lógica para eliminar y agregar la activeclase de los botones de manera adecuada. Escribe el código en la funciónrenderButtons() .


Iteración 4: Ingredientes y precios
En el lado derecho del generador de pizza, hay una sección de precios.

Escribe la función renderPrice()que:

Muestra la lista de todos los elementos seleccionados
Muestra el precio total.
