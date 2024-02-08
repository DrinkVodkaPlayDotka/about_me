<script setup lang="ts">
import {onMounted, onUnmounted, ref} from "vue";

const show = ref(false)
const showTest = () =>{
  show.value = window.scrollY>300
}
onMounted(() => {
  window.addEventListener('scroll', showTest);
});

onUnmounted(() => {
  window.removeEventListener('scroll', showTest);
});
const scrollToTop = () => {
  window.scrollTo({ top: 0, behavior: 'smooth' })
}
</script>

<template>
<header  class="fix" :class="{ 'box2': !show, 'box1': show }">
  <ol>
    <li class="me" @click="scrollToTop" >It's <span class="rgb">me</span></li>
    <li class="list">привет</li>
  </ol>

</header>
</template>

<style scoped>
@import url('https://fonts.googleapis.com/css2?family=Protest+Revolution&display=swap');
.fix {
  position: fixed;
  top: 0;
  left: 0;
}

.box1{
  margin-top: 0;
  background-color: rgba(47, 44, 44, 0.5);
  width: 100%;
  height: 10%;
}
.box2{
  margin-top: 0;
  background-color: rgba(47, 44, 44, 0);
  width: 100%;
  height: 10%;
}
ol {
  list-style-type:  none;
  display: flex;
  color:  white;



}
.me{
  font-family: 'Protest Revolution', sans-serif;
  color:  white;
  font-size: 3rem;
  user-select: none;
  cursor: pointer;
}
.list{
  text-align: center;

}
.rgb{
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