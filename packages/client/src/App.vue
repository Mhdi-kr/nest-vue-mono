<template>
    <div class="h-screen flex flex-col items-center justify-center">
        <img class="mb-4" alt="Vue logo" src="./assets/logo.png" />
        <HelloWorld msg="Client Application" />
    </div>
</template>

<script setup lang="ts">
import { onMounted } from "vue";
import HelloWorld from "./components/HelloWorld.vue";
onMounted(async (): Promise<void> => {
    // This is called when the component is mounted
    const res = await fetch("http://localhost:8090/");
    const json = await res.json();
    console.log(json);
});
</script>
