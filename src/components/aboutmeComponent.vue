<script setup lang="ts">

</script>

<template>
    <div class="container">
      <div class="box">
        <div>About me</div>
        <div>Hi, my name is Misha Stepanov,  crazy full stack web developer who wants to explore every tech stack.</div>
        <div>I go to a badass university called YSTU.</div>
        <div>My goal is to become a highly skilled web developer</div>
        <div>Here are some of the technologies I've been working with lately:</div>
      </div>
    </div>
</template>

<style scoped>
.newPage{
  padding-top: 15rem;
  color: white;
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