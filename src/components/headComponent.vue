<script setup lang="ts">
import {onMounted, onUnmounted, ref} from "vue";

const show = ref(false)
const orange_first = ref(true)
const orange_second = ref(false)
const orange_third = ref(false)

const orange_f = () => {
  orange_first.value = window.scrollY < 500;
}
const orange_s = () => {
  orange_second.value = (!orange_first.value && window.scrollY < 1250);
}
const orange_t = () => {
  orange_third.value = (!orange_first.value && !orange_second.value && window.scrollY < 2000)
}
const showTest = () => {
  show.value = window.scrollY > 300
}
onMounted(() => {
  window.addEventListener('scroll', showTest);
  window.addEventListener('scroll', orange_f);
  window.addEventListener('scroll', orange_s);
  window.addEventListener('scroll', orange_t);


});

onUnmounted(() => {  window.removeEventListener('scroll', orange_s);

  window.removeEventListener('scroll', showTest);
  window.removeEventListener('scroll', orange_f);
  window.removeEventListener('scroll', orange_s);
  window.removeEventListener('scroll', orange_t);


});
const scrollToTop = () => {
  window.scrollTo({top: 0, behavior: 'smooth'})
}
const scrollToAbout = () => {
  window.scrollTo({top: 700, behavior: 'smooth'})
}
const scrollToSkills = () =>{
  window.scrollTo({top: 1500, behavior: 'smooth'})

}
</script>

<template>
  <header class="fix" :class="{ 'box2': !show, 'box1': show }">
    <ol>
      <li class="me" @click="scrollToTop">It's <span class="rgb">me</span></li>
      <li class="list onClick" @click="scrollToTop" :class="{'orange': orange_first}">literally me</li>
      <li class="list onClick" @click="scrollToAbout" :class="{'orange': orange_second}">about me</li>
      <li class="list onClick" @click="scrollToSkills" :class="{'orange': orange_third}">Skills</li>

    </ol>

  </header>
</template>

<style scoped>
@import url('https://fonts.googleapis.com/css2?family=Protest+Revolution&display=swap');
@import url('https://fonts.googleapis.com/css2?family=Protest+Riot&display=swap');

.fix {
  position: fixed;
  top: 0;
  left: 0;
  z-index: 1002;
}

.onClick {
  cursor: pointer;

}

.box1 {
  margin-top: 0;
  background-color: rgba(47, 44, 44, 0.5);
  width: 100%;
  height: 10%;
}

.box2 {
  margin-top: 0;
  background-color: rgba(47, 44, 44, 0);
  width: 100%;
  height: 10%;
}

ol {
  list-style-type: none;
  display: flex;
  color: white;
  font-family: 'Protest Riot', sans-serif;
}

.me {
  font-family: 'Protest Revolution', sans-serif;
  color: white;
  font-size: 3rem;
  user-select: none;
  cursor: pointer;
}

.orange {
  color: #ee8241;
  cursor: pointer;


}

.list {
  margin-left: 20%;
  margin-top: 1%;
  text-align: center;

}

.rgb {
  background: linear-gradient(45deg, #e8600c 33%, #c28341 66%, #9f58c9);
  -webkit-background-clip: text;
  -webkit-text-fill-color: transparent;
  animation: colorChange 10s infinite alternate;

}

@keyframes colorChange {
  0% {
    filter: hue-rotate(0deg);
  }
  100% {
    filter: hue-rotate(360deg);
  }
}
</style>