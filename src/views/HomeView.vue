
<template>
  <div class="landing">
    <div class="hero">
      <h1 class="heading">heading</h1>
      <h3 class="subheading">subheading</h3>
      <div class="buttons-container">
        <button>button1</button>
        <button>button2</button>
      </div>
    </div>
    <div class="example-wrapper">
      <div class="example">
        <img src="../assets/logo.svg" :style="{width: '10em'}" alt="">
        <h1>example</h1>
        <p>Lorem ipsum dolor sit amet consectetur adipisicing elit. Autem, aspernatur expedita atque reprehenderit reiciendis minus eaque, dolorum, possimus tempore in voluptatibus aut ab ratione nihil id facilis. Dolore, aperiam iure!</p>
      </div>
      <div class="example">
        <img src="../assets/logo.svg" :style="{width: '10em'}" alt="">
        <h1>example</h1>
        <p>Lorem ipsum dolor sit amet consectetur adipisicing elit. Autem, aspernatur expedita atque reprehenderit reiciendis minus eaque, dolorum, possimus tempore in voluptatibus aut ab ratione nihil id facilis. Dolore, aperiam iure!</p>
      </div>
      <div class="example">
        <img src="../assets/logo.svg" :style="{width: '10em'}" alt="">
        <h1>example</h1>
        <p>Lorem ipsum dolor sit amet consectetur adipisicing elit. Autem, aspernatur expedita atque reprehenderit reiciendis minus eaque, dolorum, possimus tempore in voluptatibus aut ab ratione nihil id facilis. Dolore, aperiam iure!</p>
      </div>
      <div class="example">
        <img src="../assets/logo.svg" :style="{width: '10em'}" alt="">
        <h1>example</h1>
        <p>Lorem ipsum dolor sit amet consectetur adipisicing elit. Autem, aspernatur expedita atque reprehenderit reiciendis minus eaque, dolorum, possimus tempore in voluptatibus aut ab ratione nihil id facilis. Dolore, aperiam iure!</p>
      </div>
    </div>
  </div>
</template>

<script lang="ts">
import { defineComponent } from 'vue';

export default defineComponent({
  name: 'HomeView',
  data() {
    return {
      text: ''
    }
  }
})
</script>
<style scoped>
.hero {
  display: flex;
  flex-direction: column;
  height: 40em;
  padding-left: 10em;
  background-image: url('../assets/hero-img.jpg');
  background-position: center;
  background-size: contain;
}

.heading {
  color: white;
  margin-bottom: 0.2em;
}

.subheading {
  color: white;
  margin: 0 0 2em 0.75em;
}

.buttons-container :nth-child(2) {
  background-color: rgb(255, 153, 0);
  color: white;
  margin-left: 1em;
  padding: 15px 60px;
  border-radius: 1em;
  border: none;
  cursor: pointer;
  transition: all 0.7s;
}

.buttons-container :nth-child(1) {
  background-color: rgb(255, 255, 255);
  color: black;
  padding: 15px 60px;
  border-radius: 1em;
  border: none;
  cursor: pointer;
  transition: all 0.7s;
}

.buttons-container *:hover {
  rotate: 180deg;
}

.example {
  margin: 2em;
  width: 20em;
  display: flex;
  flex-direction: column;
  align-items: center;
  justify-content: center;
  text-align: center;
}

.example-wrapper {
  display: flex;
  flex-wrap: wrap;
  align-items: center;
  justify-content: center;
}

</style>