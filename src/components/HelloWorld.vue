<template>
  <p>Hi {{ name | fallback }}!</p>
</template>

<script>
export default {
  data() {
    return {
      name: ''
    }
  },
  filters: {
    fallback: function(name) {
      return name ? name : 'there'
    }
  }
}
</script>