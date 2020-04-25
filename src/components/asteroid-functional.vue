<script>
  export default {
    functional: true,

    name: 'Asteroid',

    props: {
      data: Object
    },

    render(h, context) {
      const data = {
        name: context.props.data.name,
        year: context.props.data.year
          ? context.props.data.year.substr(0, 4)
          : '-',
        recclass: context.props.data.recclass,
        mass: context.props.data.mass,
        location: context.props.data.geolocation
          ? context.props.data.geolocation.coordinates
          : '🚩'
      };

      function createDataEntry(key) {
        return [
          h(
            'dt',
            key.replace(/^\w/, c => c.toUpperCase())
          ),
          h('dd', data[key])
        ];
      }

      return h('li', [
        h('h2', `${data.name} - ${data.year}`),
        h('dl', [
          ...createDataEntry('recclass'),
          ...createDataEntry('mass'),
          ...createDataEntry('location')
        ])
      ]);
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
