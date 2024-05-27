<template>
  <div id="app">
    <h1>Vue Nested Components</h1>
    <div class="app-container">
      <ParentComponent>
        <!-- Ini adalah contoh penggunaan slot untuk menyisipkan data atau komponen -->
        <p>Sisipkan data atau komponen di sini</p>
      </ParentComponent>
    </div>
  </div>
</template>

<script>
import ParentComponent from './components/ParentComponent.vue';

export default {
  name: 'App',
  components: {
    ParentComponent,
  },
};
</script>


<style>
#app {
  font-family: Arial, sans-serif;
  text-align: center;
  margin-top: 50px;
}

.app-container {
  max-width: 800px;
  margin: 0 auto;
}


</style>
