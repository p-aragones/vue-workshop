<template>
    <div class="wrapper">
        <h1>heading</h1>
        <h2>heading</h2>
        <h3>heading</h3>
        <h4>heading</h4>
        <h5>heading</h5>
        <h6>heading</h6>
        <p>body</p>
        <input type="text" v-model="inputText">
        <p>{{inputText}}</p>
        <a href="https://google.com" target="_blank">link to google</a>
        <img src="../assets/logo.svg" :style="{width: '10em'}" alt="vue logo">
        <button class="test-button">button</button>
        <ul>
          <li>unordered list</li>
          <li>unordered list</li>
          <li>unordered list</li>
        </ul>
        <ol>
          <li>ordered list</li>
          <li>ordered list</li>
          <li>ordered list</li>
        </ol>
        <TestComponent  v-on:selected="changeText"></TestComponent>
        <p>{{ text }}</p>
    </div>
</template>

<script lang="ts">
import { defineComponent } from 'vue';
import TestComponent from '../components/TestComponent.vue';

export default defineComponent({
    name: "TestView",
    data() {
        return {
            inputText: "",
            text: '',
        };
    },
    components: {
        TestComponent
    },
    methods: {
      changeText(ev: any) {
        console.log(ev)
        this.text = ev;
      }
    }
})
</script>

<style>
.wrapper {
  display: flex;
  flex-direction: column;
  align-items: center;
  justify-content: center;
}

.wrapper > * {
  margin: 1em 0;
}

.test-button {
  padding: 10px 50px;
}
</style>