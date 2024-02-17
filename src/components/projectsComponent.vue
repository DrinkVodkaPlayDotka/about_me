<script setup lang="ts">
import {ref} from "vue";

let photos: string[] = ["http://kalinkovichi.globalmarket.by/wp-content/themes/globalmarket/thumb.php?src=http://kalinkovichi.globalmarket.by/wp-content/themes/globalmarket/img/default_image.jpg&w=144&h=88"];
let disc: string[] = ["Шняга шнядная,жизнь общажная", "а тут телеграм бота на c# и всяё такое"]
const currentPhoto = ref<number>(0);
const anim = ref<boolean>(false);
const checkEl = ref<boolean>(false)

const check = () => {
  checkEl.value = true
}
const checkOut = () =>{
  checkEl.value = false
}
const changePhoto = () => {
  anim.value = true
  setTimeout(() => {
    anim.value = false
    if (currentPhoto.value != photos.length - 1) {
      currentPhoto.value += 1;
    } else {
      currentPhoto.value = 0;
    }
  }, 300);
}
const changePhotoleft = () => {
  anim.value = true
  setTimeout(() => {
    anim.value = false
    if (currentPhoto.value != 0) {
      currentPhoto.value -= 1;
    } else {
      currentPhoto.value = photos.length - 1;
    }
  }, 500);
}

</script>

<template>
  <div class="container">
    <span class="proj" :class="{'proj2': checkEl}">Projects</span>
    <div class="box">
      <div @mouseover="check" @mouseout="checkOut" class="opac cont" :class="{'animation': anim == true}"
           v-for="(photo, index) in photos" :key="index">
        <img v-if="index === currentPhoto" :src="photo" :alt="'Изображение ' " :key="index"/>
        <div v-if="index === currentPhoto">{{ disc[index] }}</div>
      </div>

      <button @mouseover="check"  @mouseout="checkOut" class="btn1 tick" @click="changePhoto"> ></button>
      <button @mouseover="check"  @mouseout="checkOut" class="btn2 tick" @click="changePhotoleft"> &lt;</button>

    </div>

  </div>
</template>
<style scoped>
@import url('https://fonts.googleapis.com/css2?family=Noto+Sans+JP&family=Protest+Riot&display=swap');

.proj {
  position: absolute;
  top: calc(100% - 80% - 17%);
  left: 50%;
  transform: translateX(-50%);
  font-family: 'Protest Riot', sans-serif;

  color: #222;
  font-size: 24px;
  font-weight: bold;
  letter-spacing: 5px;
  cursor: pointer;
  text-transform: uppercase;
  transition: 0.5s;
}
.proj2{
  color: #fff;
  text-shadow: 0 0 5px #03e9f4,
  0 0 25px #03e9f4,
  0 0 50px #03e9f4,
  0 0 100px #03e9f4;
}
.proj2{
  color: #fff;
  text-shadow: 0 0 5px #03e9f4,
  0 0 25px #03e9f4,
  0 0 50px #03e9f4,
  0 0 100px #03e9f4;
  position: absolute;
  top: calc(100% - 80% - 17%);
  left: 50%;
  transform: translateX(-50%);
  font-family: 'Protest Riot', sans-serif;
  font-size: 24px;
  font-weight: bold;
  letter-spacing: 5px;
  cursor: pointer;
  text-transform: uppercase;
  transition: 0.5s;
}


.btn2 {
  opacity: 0.5;
  width: 40px;
  height: 40px;
  background-color: #808080;
  color: #fff;
  text-transform: uppercase;
  letter-spacing: 2px;
  cursor: pointer;
  border-radius: 50%;
  border: 2px dashed #808080;
  box-shadow: rgba(50, 50, 93, 0.25) 0px 2px 5px -1px, rgba(0, 0, 0, 0.3) 0px 1px 3px -1px;
  transition: .4s;
  position: absolute;
  top: 35%;
  left: 0%;
}

.btn2:hover {
  border: 2px dashed #808080;
  background-color: #fff;
  color: #808080;
}

.btn2:active {
  background-color: #87dbd0;
}

.tick {
  font-size: 20px;
}

.btn1 {
  opacity: 0.5;

  width: 40px;
  height: 40px;
  background-color: #808080;
  color: #fff;
  text-transform: uppercase;
  letter-spacing: 2px;
  cursor: pointer;
  border-radius: 50%;
  border: 2px dashed #808080;
  box-shadow: rgba(50, 50, 93, 0.25) 0px 2px 5px -1px, rgba(0, 0, 0, 0.3) 0px 1px 3px -1px;
  transition: .4s;
  position: absolute; /* позволяет задать позицию кнопки относительно родительского контейнера */
  top: 35%; /* размещаем кнопку на середине вертикали */
  right: 0%;
}

.btn1:hover {
  border: 2px dashed #808080;
  background-color: #fff;
  color: #808080;
}

.btn1:active {
  background-color: #87dbd0;
}

.container {
  position: relative;
  margin-top: 25%;
  display: flex;
  justify-content: center;
  align-items: center;
  height: 60vh;
  text-align: center;

  width: 100%;
}

@keyframes borderGlow {
  0% {
    box-shadow: 0 0 10px 5px rgba(255, 255, 255, 0.1); /* Белый с низкой прозрачностью */
  }
  25% {
    box-shadow: 0 0 10px 5px rgba(255, 255, 255, 0.3); /* Белый средней прозрачности */
  }
  50% {
    box-shadow: 0 0 10px 5px rgba(255, 255, 255, 0.5); /* Светлый белый */
  }
  75% {
    box-shadow: 0 0 10px 5px rgba(255, 255, 255, 0.7); /* Белый средней прозрачности */
  }
  100% {
    box-shadow: 0 0 10px 5px rgba(255, 255, 255, 0.8); /* Белый с низкой прозрачностью */
  }
}


.box {
  width: 20%;
  height: 80%;
  background: #808080;
  position: relative;
  border-radius: 25px;
  transition: transform 0.5s ease, transform 0.3s ease;


}

.box:hover {
  animation: borderGlow 4s forwards;
  -webkit-transform: scale(1.2);
  -ms-transform: scale(1.2);
  transform: scale(1.2) perspective(1000px) rotateX(20deg);

}


.opac {
  opacity: 1;
}

.animation {
  animation: fadeOut 0.5s forwards;
}

@keyframes fadeOut {
  from {
    opacity: 1;
  }
  to {
    opacity: 0;
  }
}

img {
  width: 100%;
  height: 400px;
  border-top-left-radius: 25px;
  border-top-right-radius: 25px;
  opacity: 1 !important;
}
</style>