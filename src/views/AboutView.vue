<template>
  <div class="card">
    <div class="face front">
      <img src="../assets/weather.jpg" alt="">
      <h3>Weather App</h3>
    </div>
    <div class="face back">
      <h3>Proyecto</h3>
      <p>Este proyecto hecho con Vue es una aplicación del clima utilizando una API e implementando nuestro previo conocimiento de los Router...</p>
      <div class="link">
        <a href="#">...</a>
      </div>
    </div>
  </div>
</template>

<style>

*{
  margin: 0;
  padding: 0;
  box-sizing: border-box;
  border-radius: 10px;
  font-family: sans-serif;
  
}

body{
  display: flex;
  align-items: center;
  justify-content: center;
  min-height: 100vh;
  background: rgb(9, 74, 136);
  
}

.card{
  position: relative;
  width: 300px;
  height: 350px;
  
  
}

.card .face{
  position: absolute;
  width: 100%;
  height: 100%;
  backface-visibility: hidden;
  border-radius: 10px;
  overflow: hidden;
  transition: .5s;
  border-radius: 10px;
  
}

.card .front{
  transform: perspective(600px) rotateY(0deg) ;
  box-shadow: 0 5px 10px #000;
}

.card .front img{
  position: absolute;
  width: 100%;
  height: 100%;
  object-fit: cover;
} 

.card .front h3{
  position: absolute;
  bottom: 0;
  width: 100%;
  height: 45px;
  line-height: 45px;
  color: #fff;
  background: rgba(0, 0, 0, .4);
  text-align: center;
}

.card .back {
  transform: perspective(600px) rotateX(180deg);
  background: rgb(3, 35, 54);
  padding: 15px;
  color: #f3f3f3;
  display: flex;
  flex-direction: column;
  justify-content: space-between;
  text-align: center;
  box-shadow: 0 5px 10px #000;
}

.card .back .link{
  border-top: solid 1px #f3f3f3;
  height: 50px;
  line-height: 50px;

}

.card .back .link a{
  color: #f3f3f3;
}

.card .back h3{
  font-size: 30px;
  margin-top: 20px;
  letter-spacing: 2px;
}

.card .back p{
  letter-spacing: 1px;
}

.card:hover .front{
  transform: perspective(600px) rotateY(180deg);
}

.card:hover .back{
  transform: perspective(600px) rotateY(360deg);
}

</style>

