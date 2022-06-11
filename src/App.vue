<script lang="ts" setup>
import { ref } from "vue";
import GitHubCorner from './components/GitHubCorner.vue';
import Footer from './components/Footer.vue';

const buttonClicks = ref(localStorage.getItem('uselesswebsite.clicks') || 0);

const increase = () => {
  localStorage.setItem('uselesswebsite.clicks', (buttonClicks.value++) + 1);
}
</script>

<template>
  <GitHubCorner />

  <h1>You clicked the button <span>{{ buttonClicks }}</span> times</h1>
  <a class="x-btn x-btn-animate" @click="increase"><span>Click</span></a>

  <Footer />
</template>