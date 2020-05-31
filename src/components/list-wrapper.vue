<template functional>
  <div>
    <ul v-if="props.listType === 'ul'">
      <slot />
    </ul>
    <ol v-if="props.listType === 'ol'">
      <slot />
    </ol>
  </div>
</template>
<script>
  export default {
    name: 'ListWrapper',
  };
</script>
