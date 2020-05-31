<template>
  <div id="app">
    <!--
      We can pass it ul without v-bind or `:`
      as it needs to be a string anyway.
    -->
    <ListWrapper listType="ul">
      <li>Wonder Woman</li>
      <li>Batman</li>
      <li>Superman</li>
      <li>Aquaman</li>
    </ListWrapper>

    <ListWrapper listType="ol">
      <li>Wonder Woman</li>
      <li>Batman</li>
      <li>Superman</li>
      <li>Aquaman</li>
    </ListWrapper>
  </div>
</template>

<script>
  import ListWrapper from './components/list-wrapper';

  export default {
    name: 'App',
    components: {
      ListWrapper,
    },
  };
</script>
