<script>
  export default {
    functional: true,
    name: 'UserAvatar',

    render(h) {
      // For Reference:
      // <div class="avatar">
      //   <figure>
      //     <img src="/avatar.png" alt="Jane Doe" />
      //   </figure>
      // </div>

      return h('div', { class: 'avatar' }, [
        h('figure', [
          h('img', {
            attrs: {
              src: '/avatar.png',
              alt: 'Jane Doe',
            },
          }),
        ]),
      ]);
    },
  };
</script>
