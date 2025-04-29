<script setup>
import TheAside from './components/Aside/TheAside.vue';
import TheContainer from './components/Container/TheContainer.vue';
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
  box-shadow: 0 4px 8px rgba(0, 0, 0, 0.2);
  color: #47516b;
}

@media screen and (max-width: 500px) {
  .cv {
    padding: 0px 0px;
    flex-direction: column;
    max-width: 100%;
  }
  
}
</style>
