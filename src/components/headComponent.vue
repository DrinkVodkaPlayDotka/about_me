<script setup lang="ts">
import {onMounted, onUnmounted, ref} from "vue";

const show = ref(false)
const orange_first = ref(true)
const orange_second = ref(false)
const orange_third = ref(false)
const orange_fourth = ref(false)
const orange_five = ref(false)
const orange_f = () => {
  orange_first.value = window.scrollY < 500;
}
const orange_s = () => {
  orange_second.value = (!orange_first.value && window.scrollY < 1250);
}
const orange_t = () => {
  orange_third.value = (!orange_first.value && !orange_second.value && window.scrollY < 2000)
}
const orange_fe = () => {
  orange_fourth.value = (!orange_first.value && !orange_second.value && !orange_third.value && window.scrollY < 3000)
}
const orange_fi = () =>{
  orange_five.value = (!orange_first.value && !orange_second.value && !orange_third.value && !orange_fourth.value && window.scrollY < 4000)

}
const showTest = () => {
  show.value = window.scrollY > 300
}
onMounted(() => {
  window.addEventListener('scroll', showTest);
  window.addEventListener('scroll', orange_f);
  window.addEventListener('scroll', orange_s);
  window.addEventListener('scroll', orange_t);
  window.addEventListener('scroll', orange_fe);
  window.addEventListener('scroll', orange_fi);


});

onUnmounted(() => {  window.removeEventListener('scroll', orange_s);

  window.removeEventListener('scroll', showTest);
  window.removeEventListener('scroll', orange_f);
  window.removeEventListener('scroll', orange_s);
  window.removeEventListener('scroll', orange_t);
  window.removeEventListener('scroll', orange_fe);
  window.removeEventListener('scroll', orange_fi);




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
const scrollToProjects = () =>{
  window.scrollTo({top: 2400, behavior: 'smooth'})

}
const scrollToCon = () =>{
  window.scrollTo({top: 3000, behavior: 'smooth'})

}
</script>

<template>
  <header class="fix" :class="{ 'box2': !show, 'box1': show }">
    <ol class="nav">

      <li class="list onClick" @click="scrollToTop" :class="{'orange': orange_first}"><a>literally me </a> </li>
      <li class="list onClick" @click="scrollToAbout" :class="{'orange': orange_second}"><a>about me </a> </li>
      <li class="list onClick" @click="scrollToSkills" :class="{'orange': orange_third}"><a>Skills </a> </li>
      <li class="list onClick" @click="scrollToProjects" :class="{'orange': orange_fourth}"><a>Projects </a> </li>
      <li class="bn39 onClick r" @click="scrollToCon"><button :class="{'orange2': orange_five}" >CONNECT</button></li>

    </ol>

  </header>
</template>

<style scoped>
@import url('https://fonts.googleapis.com/css2?family=Protest+Revolution&display=swap');
@import url('https://fonts.googleapis.com/css2?family=Protest+Riot&display=swap');
@import url('https://fonts.googleapis.com/css?family=Titillium+Web:400,600');

button{
  color: rgba(255,255,255,.5);
  left: 600%;
  border:none;
  background-color: transparent;
  font-size:30px;
  text-transform:capitalize;
  cursor:pointer;
  transform:all 0.3s;
  position:relative;
}
button:before{
  content:"";
  position :absolute;
  width:24px;
  height:24px;
  top:-5px;
  left:-5px;
  border-top:2px solid tomato;
  border-left:2px solid tomato;
  transition:all 0.25s;
}
button:hover:before ,button:hover:after{
  width:104%;
  height:110%;
}
button:after{
  content:"";
  position :absolute;
  width:24px;
  height:24px;
  bottom:-5px;
  right:-5px;
  border-bottom:2px solid tomato;
  border-right:2px solid tomato;
  transition:all 0.30s;
}
.nav {
  font-family: 'Titillium Web';
  text-transform: uppercase;
  text-align: center;
  font-weight: 600;
}

.nav * {
  box-sizing: border-box;
  transition: all .35s ease;
}

.nav li {
  display: inline-block;
  list-style: outside none none;
  margin: .5em 1em;
  paddin: 0;
}

.nav a {
  padding: .12em .8em;
  color: rgba(255,255,255,.5);
  position: relative;
  text-decoration: none;
  font-size: 20px;
}

.nav a::before,
.nav a::after {
  content: '';
  height: 14px;
  width: 14px;
  position: absolute;
  transition: all .35s ease;
  opacity: 0;
}

.nav a::before {
  content: '';
  right: 0;
  top: 0;
  border-top: 3px solid #ee8241;
  border-right: 3px solid #c28341;
  transform: translate(-100%, 50%);
}

.nav a:after {
  content: '';
  left: 0;
  bottom: 0;
  border-bottom: 3px solid #c28341;
  border-left: 3px solid #ee8241;
  transform: translate(100%, -50%)
}

.nav a:hover:before,
.nav a:hover:after{
  transform: translate(0,0);
  opacity: 1;
}

.nav a:hover {
  color: #f37123;
}
.fix {
  position: fixed;
  top: 0;
  left: 0;
  z-index: 1002;
}
.right{
  margin-right: 15%;
}
.onClick {
  cursor: pointer;
  user-select: none;
}

.box1 {
  margin-top: 0;
  background-color: rgba(47, 44, 44, 0.5);
  width: 100%;
  height: 8%;
}

.box2 {
  margin-top: 0;
  background-color: rgba(47, 44, 44, 0);
  width: 100%;
  height: 8%;
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
  margin-left: 30px;
}

.orange a{
  color: #ee8241 ;
  cursor: pointer;


}
.orange2{
  color: #f16815;
  cursor: pointer;


}
.list {
  margin-left: 5%;
  margin-top: 1%;


}

.rgb {
  background: linear-gradient(45deg, #ee8241 33%, #c28341 66%, #9f58c9);
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