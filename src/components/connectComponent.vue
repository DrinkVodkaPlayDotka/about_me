<script setup lang="ts">

</script>

<template>
  <div class="container">

    <form
        action="https://formspree.io/f/mwkgovln"
        method="POST"
    >
      <label class="input-label">
        <input type="email" name="email" class="input-field email" placeholder="Email">
      </label>
      <label class="input-label">
        <textarea name="message" class="input-field area"  placeholder="Type your message here..." ></textarea>
      </label>
      <button type="submit" class="button"><span>Send</span></button>

    </form>
  </div>
</template>

<style scoped>
.container {

  position: relative;
  margin-top: 10%;
  margin-left: -10%;
  display: flex;
  justify-content: center;
  align-items: center;
  height: 60vh;
  text-align: center;
  width: 100%;
}

.input-label {
  display: block;
  margin-bottom: 1rem;
}
.input-field.email {
  height: 2rem;
  width: 250px;
  margin-left: -48%;
}
.input-field.area {
  height: 10rem;
  width: 500px;
}
.input-field {
  width: 100%;
  padding: 0.5rem;
  border: 1px solid #ccc;
  border-radius: 4px;
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
