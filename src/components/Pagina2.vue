<template>
  <div>
    <p>CAROUSEL</p>
    <div class="sli">
      <ul class="slider">
        <li id="slide1" >Inicio del Slider</li>
        <li id="slide2">Parez que funciona</li>
        <li id="slide3">Pero aun me queda mucho por aprender</li>
        <li id="slide4">Se que deberia haberlo puesto en Inglés</li>
        <li id="slide5">Pero no tengo tanta práctica</li>
      </ul>
      <nav>
    <ul class="menu">
        <li><a href="#slide1">Diapositiva 1</a></li>
        <li><a href="#slide2">Diapositiva 2</a></li>
        <li><a href="#slide3">Diapositiva 3</a></li>
        <li><a href="#slide4">Diapositiva 4</a></li>
        <li><a href="#slide5">Diapositiva 5</a></li>
</ul>
</nav>
   </div>
 </div>
</template>

<script>
export default {
  name: 'CAROUSEL'
}
</script>
<style scoped>
ul, li {
    padding: 0;
    margin: 0;
    list-style: none inside;
}
ul.slider {
    position:relative; /*Necesitamos que el ul sea relativo*/
}
ul.slider li {
  width: 55vw;
  height:55vh;
    opacity: 0; /*Ocultamos todos los <li>*/
    transition: opacity 1.5s;
    position: absolute; /*Posicionamos en absoluto los <li>*/
    left: -70px;
    top: -3rem;
    margin:60px;
    padding:60px;
    border:10px solid red;
    background:#fff;
}
ul.slider li:first-child {
    opacity: 1; /*Mostramos el primer <li>*/
}
ul.slider li:target {
    opacity: 1; /*Mostramos el <li> al que apunta el enlace*/
}
nav {
    position:relative;
    top:200px;
    left:50px;
}

body, html {
    padding: 0;
    margin: 0;
    width: 100vw;
    height: 100vh;
    overflow:hidden;
}

ul, li {
    box-sizing: border-box;
}

ul.slider {
    padding: 30px;
}

#slide1 {
    color: rgb(60, 11, 88);
    background-image: url("https://lafrikileria.com/21757-large_default/pack-chapas-bola-de-dragon.jpg");
    }

#slide2 {
    background-color: #65bce8;
    color: #00324b;
}

#slide3 {
    background-color: #f90;
    color: #00324b;
}

#slide4 {
    background-color: #00324b;
    color: #65bce8;
}

#slide5 {
    background-color: #65bce8;
    color: #00324b;
    background-image: url("https://elcinefil.cat/wp-content/uploads/2017/07/E3B.jpg");
}

nav {
    width: 100vw;
    position: absolute;
    top: auto;
    right: 0;
    bottom: 0;
    left: 0;
    background: #f1f2f3;
}

nav ul {
    display: flex;
    justify-content: space-around;
    flex-wrap: wrap;
}

nav ul li {
    display: flex;
    flex-grow: 1;
    flex-wrap: wrap;
    box-sizing: border-box;
}

nav a {
    font-size: calc( 1.2rem + 1vw );
    text-decoration: none;
    font-weight: bold;
    color: #00324b;
    line-height: 1.8;
    flex-grow: 1;
    text-align: center;
    border-top: 5px solid #00324b;
    border-right: 1px solid #00324b;
    flex-wrap: wrap;
    position: relative;
}

.nav li:last-child a {
    border-right: 0;
}

.nav a:hover {
    background-color: #00324b;
    color: #fff;
    border-top-color: #65bce8;
}

.nav a:active {
    border-top-color: #f90;
    background: #f90;
    color: #00324b;
}

.sli {
  max-width: 800px;
  margin: 0 auto;

}

</style>
