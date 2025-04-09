<script setup>
import TheAside from './components/TheAside.vue';
import TheContainer from './components/TheContainer.vue';
</script>

<template>
    <div class="cv">
      <TheAside></TheAside>
      <TheContainer></TheContainer>
    </div>
</template>

<style scoped>
.main {
  display: flex;
  justify-content: center;
  align-items: center;
  background-color: antiquewhite;
  color: #47516b;
  height: 100vh;
}
.cv {
  display: flex;
  width: 100%;
  max-width: 1200px;
  height: 100%;
  /*background-color: #fff;*/
  box-shadow: 0 4px 8px rgba(0, 0, 0, 0.2);
  /*padding: 48px;*/
  color: #47516b;
}
</style>
