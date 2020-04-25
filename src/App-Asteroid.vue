<template>
  <div id="app">
    <h1>Vue App</h1>
    <ul>
      <Asteroid
        v-for="asteroid in asteroids"
        :key="asteroid.id"
        :data="asteroid"
      />
    </ul>
  </div>
</template>

<script>
  const asteroids = require('./asteroids.json'); // 1K Items
  import Asteroid from './components/asteroid-functional';

  export default {
    name: 'App',

    data() {
      return {
        asteroids,
      };
    },

    components: {
      Asteroid,
    },

    created() {
      console.time('rendering');
    },

    mounted() {
      console.timeEnd('rendering');
    },
  };
</script>
