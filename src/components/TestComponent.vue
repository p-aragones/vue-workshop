<template>
    <div class="wrapper">
        <div class="item-container" v-for="item in items" :key="item.id">
            <button @click="changeText(item)" class="item-button">{{ item.text }}</button>
        </div>
    </div>
        
</template>

<script lang="ts">
import { defineComponent } from 'vue';

export default defineComponent({
    name: 'TestComponent',
    data() {
        return {
            items: [
                {
                    id: 1,
                    text: 'epitech'
                },
                {
                    id: 2,
                    text: 'vue'
                },
                {
                    id: 3,
                    text: 'JavaScript'
                },
                {
                    id: 4,
                    text: 'frontend'
                },
                {
                    id: 5,
                    text: 'pol'
                },
            ]
        }
    },
    methods: {
        changeText(item: any) {
            this.$emit("selected", item.text);
        }
    }
})
</script>

<style scoped>
.wrapper {
    display: flex;
    flex-direction: row;
    flex-wrap: wrap;
    width: 20em;
    background-color: red;
    border-radius: 2em;
    -webkit-box-shadow: 2px 10px 55px 0px rgba(0,0,0,0.75);
    -moz-box-shadow: 2px 10px 55px 0px rgba(0,0,0,0.75);
    box-shadow: 2px 10px 55px 0px rgba(0,0,0,0.75);
}

.item-container {
    width: fit-content;
    margin: 2em;
}

.item-button {
    padding: 2em;
    cursor: pointer;
    transition: all 0.5s;
}

.item-button:hover {
    background-color: aquamarine;
}
</style>