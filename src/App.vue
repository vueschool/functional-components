<template>
  <div id="app">
    <h1>User Card</h1>
    <div class="center">
      <div class="card">
        <div class="additional">
          <figure class="avatar">
            <img :src="user.avatar" :alt="user.name" />
          </figure>
        </div>
        <div class="more-info">
          <h1>{{ user.name }}</h1>
          <h3>{{ user.role }}</h3>
          <p>{{ user.bio }}</p>
        </div>
      </div>
      <!-- .card End -->
      <!-- <UserCard :user="user" /> -->
    </div>
  </div>
</template>

<script>
  // import UserCard from './components/user-card'

  export default {
    name: 'App',

    data() {
      return {
        user: {
          name: 'Jane Doe',
          role: 'Staff Engineer',
          avatar: 'https://randomuser.me/api/portraits/women/26.jpg',
          bio:
            'Candy canes sweet roll pudding liquorice jelly beans brownie powder pie. Pudding powder marshmallow sugar plum dessert pastry jelly-o pastry marzipan. Jelly topping biscuit jelly beans cookie cheesecake.',
        },
      };
    },

    components: {
      // UserCard,
    },
  };
</script>
