<template functional>
  <div class="card">
    <div class="additional">
      <figure class="avatar">
        <img :src="props.user.avatar" :alt="props.user.name" />
      </figure>
    </div>
    <div class="more-info">
      <h1>{{ props.user.name }}</h1>
      <h3>{{ props.user.role }}</h3>
      <p>{{ props.user.bio }}</p>
    </div>
  </div>
</template>
