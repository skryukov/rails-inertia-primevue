<template>
  <Head title="Inertia + Vite Ruby + Vue Example" />

  <div class="root">
    <h1 class="text-[3.2em] leading-[1.1]">Hello {{ name }}!</h1>

    <div>
      <a href="https://inertia-rails.dev" target="_blank">
        <img class="logo" :src="inertiaSvg" alt="Inertia logo" />
      </a>
      <a href="https://vite-ruby.netlify.app" target="_blank">
        <img class="logo vite" :src="viteRubySvg" alt="Vite Ruby logo" />
      </a>
      <a href="https://vuejs.org" target="_blank">
        <img class="logo vue" :src="vueSvg" alt="Vue logo" />
      </a>
    </div>

    <h2 class="h2">Inertia + Vite Ruby + Vue</h2>

    <div class="card">

      <Button @click="count++" raised color="primary" >
        count is: {{ count }}

      </Button>
      <p>
        Edit <code>app/frontend/pages/InertiaExample.vue</code> and save to test
        HMR
      </p>
    </div>
    <p class="readTheDocs">
      Click on the Inertia, Vite Ruby, and Vue logos to learn more
    </p>
  </div>
</template>

<script setup lang="ts">
import { Head } from '@inertiajs/vue3'
import { ref } from 'vue'

import inertiaSvg from '/assets/inertia.svg'
import viteRubySvg from '/assets/vite_ruby.svg'
import vueSvg from '/assets/vue.svg'

defineProps({
  name: String,
})

const count = ref(0)
</script>

<style scoped>
.root {
  font-family: Inter, system-ui, Avenir, Helvetica, Arial, sans-serif;
  line-height: 1.5;
  font-weight: 400;
  color: #213547;
  background-color: #ffffff;
  max-width: 1280px;
  margin: 0 auto;
  padding: 2rem;
  text-align: center;
}


.h2 {
  font-size: 2.6em;
  line-height: 1.1;
}


.logo {
  display: inline-block;
  height: 6em;
  padding: 1.5em;
  will-change: filter;
  transition: filter 300ms;
}
.logo:hover {
  filter: drop-shadow(0 0 2em #646cffaa);
}
.logo.vite:hover {
  filter: drop-shadow(0 0 2em #e4023baa);
}
.logo.vue:hover {
  filter: drop-shadow(0 0 2em #41b883aa);
}

.card {
  padding: 2em;
}

.readTheDocs {
  color: #888;
}
</style>
