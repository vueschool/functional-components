<template>
  <li>
    <h2>{{ name }} - {{ year }}</h2>
    <dl>
      <dt>Recclass</dt>
      <dd>{{ recclass }}</dd>

      <dt>Mass</dt>
      <dd>{{ mass }}</dd>

      <dt>Location</dt>
      <dd>{{ geolocation }}</dd>
    </dl>
  </li>
</template>

<script>
  export default {
    name: 'Asteroid',

    props: {
      data: Object
    },

    data() {
      return {
        name: this.data.name,
        year: this.data.year ? this.data.year.substr(0, 4) : '-',
        recclass: this.data.recclass,
        mass: this.data.mass,
        geolocation: this.data.geolocation
          ? this.data.geolocation.coordinates
          : '🚩'
      };
    }
  };
</script>

<style scoped>
  li {
    list-style-type: '☄️';
  }

  dt {
    font-weight: bold;
  }
</style>
