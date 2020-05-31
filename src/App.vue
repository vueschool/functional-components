<template>
  <div id="app">
    <UserAvatar />

    <!-- <h1>User Card</h1>
    <div class="center">
      <UserCard
        :user="user"
        @click.native="nameAlert(user.name)"
        @contact="contactUser(user.name)"
      >
        <template #body
          ><strong>{{ user.bio }}</strong></template
        >
      </UserCard>
    </div> -->
  </div>
</template>

<script>
  // import UserCard from './components/user-card';
  import UserAvatar from './components/user-avatar';

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

    methods: {
      nameAlert(name) {
        alert(`Clicked on ${name}`);
      },

      contactUser(name) {
        alert(`Contacting ${name}`);
      },
    },

    components: {
      // UserCard,
      UserAvatar,
    },
  };
</script>
