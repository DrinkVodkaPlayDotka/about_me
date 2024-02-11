<script setup lang="ts">
import {ref} from "vue";

let photos: string[] = ["https://img.freepik.com/free-photo/web-template-website-design-concept_53876-125608.jpg", "https://thumb.tildacdn.com/tild3061-3934-4461-a265-333735323466/-/resize/824x/-/format/webp/Smartiqa_Automation_.png", "https://encrypted-tbn0.gstatic.com/images?q=tbn:ANd9GcRKfAUssiqkUNJvIPed8EhCg8mHgToqiosaz9fw2QRABQ&s"];
const currentPhoto = ref<number>(0);

const changePhoto = () =>{
  if (currentPhoto.value != photos.length-1){
    currentPhoto.value +=1;
  }
  else {
    currentPhoto.value = 0;
  }
}

</script>

<template>
<div class="container">
  <div class="box">
    <BCarousel controls indicators ride="carousel">
      <BCarouselSlide img-src="https://picsum.photos/1024/480/?image=13" caption="Первый слайд: описание первого изображения" />
      <BCarouselSlide img-src="https://picsum.photos/1024/480/?image=14" caption="Второй слайд: описание второго изображения" />
      <BCarouselSlide img-src="https://picsum.photos/1024/480/?image=15" caption="Третий слайд: описание третьего изображения" />
    </BCarousel>

  </div>
</div>
</template>

<style scoped>
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
.box{
  width: 30%;
  height: 100%;
  background: white;
}
img{
  width: 100%;
  height: 400px;
}


</style>