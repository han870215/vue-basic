<template>
  <div>
    <div :class="{ 'text-red': isError, active: isActice }">class binding</div>
  </div>
</template>
<script>
export default {
  components: {},
  data() {
    return {
      isActice: true,
      isError: true
    }
  },
  setup() {},
  created() {},
  mounted() {},
  unmounted() {},
  methods: {}
}
</script>
<style scoped>
.active {
  background-color: greenyellow;
  font-weight: bold;
}
.text-red {
  color: red;
}
</style>
