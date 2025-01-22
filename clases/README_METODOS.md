# Resumen de métodos para acceder, recuperar y modificar elementos del DOM

## document.getElementById

- let variable = document.getElementById('variable'); --> accede al objeto a traves de <un ID>
- console.log(variable) --> accede al objeto

## innerHTML

- console.log(variable.innerHTML) --> accede al valor del objeto
- variable.innerHTML = "nuevo valor" --> modificar el valor del objeto

## getElementsByTagName('tag')

- let variableParrafos = document.getElementsByTagName('p'); --> accede a todos los elementos de <misma etiqueta> y crea un array

- variableParrafos.lenght -- > método para ver la cantidad de elementos en la lista

- for(let i=0; i<variableParrafos.length;i++){
  console.log(`${i} - ${parrafos[i].innerHTML}`)}; --> recorrer la lista Y acceder al valor de cada elementi

//sintáxis más sencilla

- for(parrafo of variableParrafos) {
  console.log(`${parrafo.innerHTML}`)
  }

## document.getElementsByClassName('class')

- let elementos = document.getElementsByClassName('azul');
  console.log( `No. elementos: ${elementos.length}`); --> accede a través de una misma clase de CSS

- for(let elemento of elementos){
  console.log(`${elemento.innerHTML}`);
  }

## querySelectorAll("clase")

let elementos = document.querySelectorAll('azul');
console.log( `No. elementos: ${elementos.length}`);
for(let elemento of elementos){
console.log(`${elemento.innerHTML}`);
}

## querySelectorAll("etiqueta.clase")

let elementos = document.querySelectorAll('p.azul');
console.log( `No. elementos: ${elementos.length}`);
for(let elemento of elementos){
console.log(`${elemento.innerHTML}`);
}

## document.forms['id del elemento html'];

- let formulario = document.forms['id del elemento html'];

let texto = '';

for(let elemento of formulario){
texto += elemento.value + '<br/>';
}

document.getElementById('valores').innerHTML = texto;

///recuperamos los valores individualmente sin utilizar un ciclo for

- let formulario = document.forms['idformulario'];
- let texto = '';
- let variable1 = formulario['id1'];
- let variable2 = formulario['id2'];

texto = nombre.value + '<br/>' + apellido.value;

document.getElementById('valores').innerHTML = texto;

# document.write("envío un mensaje al html") ---> sin utilizar el html, pero atenciión que puede sobreescribir cualquier estructura previa.
