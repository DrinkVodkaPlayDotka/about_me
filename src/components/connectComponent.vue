<script setup lang="ts">

</script>

<template>

  <div class="container">
    <span class="con">Connect with me</span>
    <form
        action="https://formspree.io/f/mwkgovln"
        method="POST"
    >
      <label class="input-label">
        <input type="email" name="email" class="input-field email" placeholder="Email">
      </label>
      <label class="input-label">
        <textarea name="message" type="message" class="input-field area"  placeholder="Type your message here..." ></textarea>
      </label>
      <button type="submit" class="button"><span>Send</span></button>

    </form>
    <span class="line"></span>

  </div>
</template>

<style scoped>
.list{
  position: absolute;
  left: 130vh;
  bottom: 20vh;
  list-style:none;

}
li{
  list-style:none;

}


.con {
  position: absolute;
  top: calc(100% - 80% - 17%);
  left: 50%;
  transform: translateX(-50%);
  font-size: 4vh;
  font-family: 'Space Mono', monospace;
  color: #f8f5f5;
  animation: slideAndColorChange 1.5s infinite;
}

.container {

  position: relative;
  margin-top: 10%;
  display: flex;
  justify-content: center;
  align-items: center;
  height: 60vh;
  text-align: center;
  width: 100%;
  box-shadow: 0 0 20px rgba(0, 0, 0, 0.2); /* Горизонтальное смещение, вертикальное смещение, размытие, цвет */
  transition: box-shadow 0.3s ease ,transform 0.3s ease;
}

.container:hover {
  box-shadow: 0 0 20px rgba(255, 165, 0, 0.7); /* оранжевая тень */
  transform: scale(0.95); /* увеличение размера контейнера при наведении */
  transition: box-shadow 0.3s ease, transform 0.3s ease; /* добавление плавного перехода */
  border-radius: 10px; /* добавление скругленных углов */
}


.li{
  margin-bottom: 5vh;
}
.input-label {
  display: block;
  margin-bottom: 1rem;
}
.input-field.email {
  height: 2rem;
  width: 250px;
  color: #FFA500;
  margin-left: -48%;
}
.input-field.area {
  height: 10rem;
  width: 500px;
  color: #FFA500;


}
.input-field {
  width: 100%;
  padding: 0.5rem;
  border: 3px solid #FFA500;
  border-radius: 4px;
  background-color:transparent;
  color: white;
  transition: box-shadow 0.3s ease;

}
.input-field:hover{
  box-shadow:
      rgba(255, 165, 0, 0.4) 0px 2px 4px,
      rgba(255, 165, 0, 0.3) 0px 7px 13px -3px,
      rgba(255, 165, 0, 0.2) 0px -3px 0px inset;
}
.line{
  position: absolute;
  width: 5px;
  height: 35vh;
  right: 30%;
  background-image: linear-gradient(to bottom, #ffffff, #cccccc, #ffa500); /* Градиентный фон */
  animation: colorChange 10s infinite alternate;

}

input[type="email"]::placeholder {
    color: #FFA500;
    font-family:  monospace;
    outline:none;
}
textarea[type="message"]::placeholder {
  color: #FFA500;

}
:active, :hover, :focus {
  outline: 0;
  outline-offset: 0;
}
@keyframes colorChange {
  0% {
    filter: hue-rotate(0deg);
  }
  100% {
    filter: hue-rotate(360deg);
  }
}
button {
  position: relative;
  display: flex;
  justify-content: center;
  align-items: center;
  border-radius: 5px;
  background: #183153;
  font-family: "Montserrat", sans-serif;
  box-shadow: 0px 6px 24px 0px rgba(0, 0, 0, 0.2);
  overflow: hidden;
  cursor: pointer;
  border: none;
  width: 100%;
}

button:after {
  content: " ";
  width: 0%;
  height: 100%;
  background: #FFA500;
  position: absolute;
  transition: all 0.4s ease-in-out;
  right: 0;
}

button:hover::after {
  right: auto;
  left: 0;
  width: 100%;
}

button span {
  text-align: center;
  text-decoration: none;
  width: 100%;
  padding: 18px 25px;
  color: #fff;
  font-size: 1.125em;
  font-weight: 700;
  letter-spacing: 0.3em;
  z-index: 20;
  transition: all 0.3s ease-in-out;
}

button:hover span {
  color: #183153;
  animation: scaleUp 0.3s ease-in-out;
}

@keyframes scaleUp {
  0% {
    transform: scale(1);
  }

  50% {
    transform: scale(0.95);
  }

  100% {
    transform: scale(1);
  }
}

</style>
