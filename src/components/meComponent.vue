<template>
  <div class="container">
    <div class="box">
      <span class="hi-text" @mouseover="changeText"> {{ text }} <span class="smiley">{{smiley}}</span>. I'm  </span>
      <div class="pad name-text" @mouseover="changeText">Misha Stepanov.</div>
      <div class="pad a1-text">With
        <a class="disable-link" href="https://vuejs.org/"  target="_blank">
        <span class="gradient-text-vue">VueJS</span> </a> and
        <a class="disable-link" href="https://fastapi.tiangolo.com/"  target="_blank">
        <span class="gradient-text-fast">FastAPI</span>
        </a>
      </div>

        <div class="pad a2-text"> I create interfaces that make the user experience more enjoyable than browsing kitties on the internet.</div>
       <div class="a3-text">Let me turn your project into a quiet paradise for your eyes and fingers.</div>
    </div>
  </div>
</template>

<script setup lang="ts">
import { ref } from "vue";

const text = ref('Hey, everybody');
const smiley = ref('👋');

const changeText = () =>  {
  if (text.value == 'Hey, everybody') {
    smiley.value = '👋'
    text.value = 'Hello, friends'
  } else {
    text.value = 'Hey, everybody'
    smiley.value = '👋🏿'
  }
}
</script>

<style scoped>
@import url('https://fonts.googleapis.com/css2?family=Montserrat+Alternates:wght@800&display=swap');
@import url(https://fonts.googleapis.com/css?family=Rubik+One&subset=latin,cyrillic);

@font-face {
  font-family: 'Space Mono';
  src: url('https://fonts.gstati  c.com/s/spacemono/v5/i7dPIFZifjKcF5UAWdDRaPpZYgMmQxc.woff2') format('woff2');
}
.disable-link{
  text-decoration: none;
}
@keyframes hoverInAnimation {
  0% {
    font-size: 50px;
  }
  100% {
    font-size: 70px;
  }
}

@keyframes hoverOutAnimation {
  0% {
    font-size: 70px;
  }
  100% {
    font-size: 50px;
  }
}

.gradient-text-vue {
  font-family: 'Rubik One', sans-serif;
  font-size: 50px;
  text-transform: uppercase;
  background: linear-gradient(45deg, #20c07d 33%, #499eb7 66%, #00ffa6);
  -webkit-background-clip: text;
  -webkit-text-fill-color: transparent;
  color: #0B2349;
  transition: font-size 0.3s ease; /* Добавляем переход для изменения размера шрифта */

}

.gradient-text-vue:hover {
  font-size: 60px;
}


.gradient-text-fast {
  font-family: 'Rubik One', sans-serif;
  font-size: 50px;
  text-transform: uppercase;
  background: linear-gradient(135deg, #ff6b6b, #790c5a);
  -webkit-background-clip: text;
  -webkit-text-fill-color: transparent;
  color: #0B2349;
  transition: font-size 0.3s ease; /* Добавляем переход для изменения размера шрифта */

}

.gradient-text-fast:hover {
  font-size: 60px;
}

.hi-text {
  font-family: 'Space Mono', monospace;
  color: #5da1ff;
}
.pad{
  margin-left: 10px;
  padding-bottom: 20px;

}

.a3-text{
  font-size: 1vh;
  margin-left: 10px;

  font-family: 'Space Mono', monospace;
  color: #5da1ff;
}
.a1-text{
  font-size: 4vh;
  font-family: 'Montserrat Alternates', sans-serif;
  color: #c9c7c7;
}
.a2-text{
  font-size: 2vh;
  font-family: 'Space Mono', monospace;
  color: #c9c7c7;
}
.name-text{
  margin-top: 20px;
  font-size: 6vh;
  font-family: 'Montserrat Alternates', sans-serif;
  color: #e8e5e5;
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
</style>
