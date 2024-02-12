<script setup lang="ts">
import {ref} from "vue";

let photos: string[] = ["https://img.freepik.com/free-photo/web-template-website-design-concept_53876-125608.jpg", "https://thumb.tildacdn.com/tild3061-3934-4461-a265-333735323466/-/resize/824x/-/format/webp/Smartiqa_Automation_.png", "https://encrypted-tbn0.gstatic.com/images?q=tbn:ANd9GcRKfAUssiqkUNJvIPed8EhCg8mHgToqiosaz9fw2QRABQ&s"];
let disc: string[] = ["Писал пиццерию с испольвонаием всякой шняги и т.д","писал сайт типо что-то в духе брони отелей", "а тут телеграм бота на c# и всяё такое"]
const currentPhoto = ref<number>(0);
const anim = ref<boolean>(false);

const changePhoto = () => {
  anim.value = true
  setTimeout(() => {
    anim.value = false
    if (currentPhoto.value != photos.length - 1) {
      currentPhoto.value += 1;
    } else {
      currentPhoto.value = 0;
    }
  }, 500);
}
const changePhotoleft = () => {
  anim.value = true
  setTimeout(() => {
    anim.value = false
    if (currentPhoto.value != 0) {
      currentPhoto.value -= 1;
    } else {
      currentPhoto.value =  photos.length - 1;
    }
  }, 500);
}

</script>

<template>
  <div class="container">
    <div class="box" >
      <div  class="opac cont" :class="{'animation': anim == true}"
            v-for="(photo, index) in photos" :key="index">
        <img v-if="index === currentPhoto" :src="photo" :alt="'Изображение ' " :key="index"/>
        <div  v-if="index === currentPhoto">{{disc[index]}}</div>
      </div>

      <button class="btn1 tick" @click="changePhoto"> > </button>
      <button  class="btn2 tick" @click="changePhotoleft"> &lt; </button>

    </div>

  </div>
</template>
<style scoped>
.btn2 {
  width: 40px;
  height: 40px;
  background-color: #00BFA6;
  color: #fff;
  text-transform: uppercase;
  letter-spacing: 2px;
  cursor: pointer;
  border-radius: 50%;
  border: 2px dashed #00BFA6;
  box-shadow: rgba(50, 50, 93, 0.25) 0px 2px 5px -1px, rgba(0, 0, 0, 0.3) 0px 1px 3px -1px;
  transition: .4s;
  position: absolute;
  top: 35%;
  left: 0%;
}

.btn2:hover {
  border: 2px dashed #00BFA6;
  background-color: #fff;
  color: #00BFA6;
}

.btn2:active {
  background-color: #87dbd0;
}
.tick{
  font-size: 20px;
}
.btn1 {
  width: 40px;
  height: 40px;
  background-color: #00BFA6;
  color: #fff;
  text-transform: uppercase;
  letter-spacing: 2px;
  cursor: pointer;
  border-radius: 50%;
  border: 2px dashed #00BFA6;
  box-shadow: rgba(50, 50, 93, 0.25) 0px 2px 5px -1px, rgba(0, 0, 0, 0.3) 0px 1px 3px -1px;
  transition: .4s;
  position: absolute; /* позволяет задать позицию кнопки относительно родительского контейнера */
  top: 35%; /* размещаем кнопку на середине вертикали */
  right: 0%;
}

.btn1:hover {
  border: 2px dashed #00BFA6;
  background-color: #fff;
  color: #00BFA6;
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
.box {
  width: 30%;
  height: 100%;
  background: white;
  position: relative;
}



.opac {
  opacity: 1;
}
.animation {
  animation: fadeOut 0.5s forwards; /* применяем анимацию fadeOut */
}

@keyframes fadeOut {
  from {
    opacity: 1;
  }
  to {
    opacity: 0;
  }
}
img{
  width: 100%;
  height: 400px;
}
</style>