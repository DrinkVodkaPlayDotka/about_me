<script setup lang="ts">

</script>

<template>
    <div class="container">
      <div class="box">
        <div class="a1-text pad">About me</div>
        <img class="me" src="/assets/me/photo_2022-11-20_21-43-10.jpg" alt="Описание изображения">
        <div class="square"></div>
        <div class="a2-text pad">Hi, my name is Misha Stepanov,<br>
          crazy full stack web developer who wants to explore every tech stack.</div>
        <div class="a2-text pad">I go to a badass university called <span class="YSTU">YSTU </span>.</div>
        <div class="a2-text pad">My goal is to become a highly skilled web developer</div>
        <div class="a2-text pad">Here are some of the technologies I've been working with lately:</div>
        <svg class="svgs" viewBox="0 -52.5 256 256" version="1.1" xmlns="http://www.w3.org/2000/svg" xmlns:xlink="http://www.w3.org/1999/xlink" preserveAspectRatio="xMidYMid" fill="#000000" transform="rotate(270)"><g id="SVGRepo_bgCarrier" stroke-width="0"></g><g id="SVGRepo_tracerCarrier" stroke-linecap="round" stroke-linejoin="round"></g><g id="SVGRepo_iconCarrier"> <g> <path d="M256,1.58059746e-06 L164.571429,150.862381 L145.602407,119.643444 L217.609266,1.58059746e-06 L256,1.58059746e-06 Z M47.2036726,-9.99999969e-07 L91.8776944,73.3667563 L136.530102,-9.99999997e-07 L181.894737,-9.99999997e-07 L90.9473686,150.068366 L-9.18903726e-15,-9.99999969e-07 L47.2036726,-9.99999969e-07 Z" fill="#10E7FF"> </path> </g> </g></svg>
        <span>Axios#</span>
        <svg class="svgs" viewBox="0 -52.5 256 256" version="1.1" xmlns="http://www.w3.org/2000/svg" xmlns:xlink="http://www.w3.org/1999/xlink" preserveAspectRatio="xMidYMid" fill="#000000" transform="rotate(270)"><g id="SVGRepo_bgCarrier" stroke-width="0"></g><g id="SVGRepo_tracerCarrier" stroke-linecap="round" stroke-linejoin="round"></g><g id="SVGRepo_iconCarrier"> <g> <path d="M256,1.58059746e-06 L164.571429,150.862381 L145.602407,119.643444 L217.609266,1.58059746e-06 L256,1.58059746e-06 Z M47.2036726,-9.99999969e-07 L91.8776944,73.3667563 L136.530102,-9.99999997e-07 L181.894737,-9.99999997e-07 L90.9473686,150.068366 L-9.18903726e-15,-9.99999969e-07 L47.2036726,-9.99999969e-07 Z" fill="#10E7FF"> </path> </g> </g></svg>
        <span>Pinia</span>
        <svg class="svgs" viewBox="0 -52.5 256 256" version="1.1" xmlns="http://www.w3.org/2000/svg" xmlns:xlink="http://www.w3.org/1999/xlink" preserveAspectRatio="xMidYMid" fill="#000000" transform="rotate(270)"><g id="SVGRepo_bgCarrier" stroke-width="0"></g><g id="SVGRepo_tracerCarrier" stroke-linecap="round" stroke-linejoin="round"></g><g id="SVGRepo_iconCarrier"> <g> <path d="M256,1.58059746e-06 L164.571429,150.862381 L145.602407,119.643444 L217.609266,1.58059746e-06 L256,1.58059746e-06 Z M47.2036726,-9.99999969e-07 L91.8776944,73.3667563 L136.530102,-9.99999997e-07 L181.894737,-9.99999997e-07 L90.9473686,150.068366 L-9.18903726e-15,-9.99999969e-07 L47.2036726,-9.99999969e-07 Z" fill="#10E7FF"> </path> </g> </g></svg>
        <span>Postgres</span>
        <svg class="svgs" viewBox="0 -52.5 256 256" version="1.1" xmlns="http://www.w3.org/2000/svg" xmlns:xlink="http://www.w3.org/1999/xlink" preserveAspectRatio="xMidYMid" fill="#000000" transform="rotate(270)"><g id="SVGRepo_bgCarrier" stroke-width="0"></g><g id="SVGRepo_tracerCarrier" stroke-linecap="round" stroke-linejoin="round"></g><g id="SVGRepo_iconCarrier"> <g> <path d="M256,1.58059746e-06 L164.571429,150.862381 L145.602407,119.643444 L217.609266,1.58059746e-06 L256,1.58059746e-06 Z M47.2036726,-9.99999969e-07 L91.8776944,73.3667563 L136.530102,-9.99999997e-07 L181.894737,-9.99999997e-07 L90.9473686,150.068366 L-9.18903726e-15,-9.99999969e-07 L47.2036726,-9.99999969e-07 Z" fill="#10E7FF"> </path> </g> </g></svg>
          <span>Docker</span>

      </div>
    </div>
</template>

<style scoped>
@import url('https://fonts.googleapis.com/css2?family=Montserrat+Alternates:wght@800&display=swap');
@import url(https://fonts.googleapis.com/css?family=Rubik+One&subset=latin,cyrillic);

@font-face {
  font-family: 'Space Mono';
  src: url('https://fonts.gstati  c.com/s/spacemono/v5/i7dPIFZifjKcF5UAWdDRaPpZYgMmQxc.woff2') format('woff2');
}
.pad{
  margin-left: 10px;
  padding-bottom: 20px;

}
.newPage{
  padding-top: 15rem;
  color: white;

}
.YSTU{
  font-size: 25px;
  font-family: 'Space Mono';

  text-transform: uppercase;
  background: linear-gradient(45deg, #0c80c7 33%, #e8600c 66%, #c28341);
  -webkit-background-clip: text;
  -webkit-text-fill-color: transparent;
}
.svgs{
  width: 2vh;
  height: auto;
}
.a1-text{
  font-size: 4vh;
  font-family: 'Space Mono', monospace;
  color: #f8f5f5;
}

.a2-text{
  font-size: 1.5vh;
  font-family: 'Space Mono', monospace;
  color: #c9c7c7;
}
.container {
  display: flex;
  justify-content: center;
  align-items: center;
  height: 90vh; /* Высота 70% от высоты экрана */
  width: 90vw; /* Ширина 90% от ширины экрана */
}

.box {
  width: 50%;
  height: 50%; /* Высота 70% от высоты родительского контейнера */
}
.me{
  position: absolute;
  top: 120%;
  left: 60%;
  height: 30vh;
  width: auto;
  border-radius: 5%;
  z-index: 1001;

}

.square {
  position: absolute;
  top: 122%; /* Расположение фото относительно верхнего края */
  left: 62%;
  z-index: 1000;
  width: 30vh;
  border-radius: 5%;
  border: 2px solid #5da1ff;

  height: 30vh;
  transition: transform 0.3s ease;

}
.me:hover + .square {
  transform: translate(-4%, -4%);
}
</style>