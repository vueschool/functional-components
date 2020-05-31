<script>
  export default {
    name: 'ListWrapper',

    functional: true,

    render(h, context) {
      return h(context.props.listType, context.children);
    },
  };
</script>
