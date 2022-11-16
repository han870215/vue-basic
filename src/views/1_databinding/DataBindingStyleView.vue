<template>
  <div>
    <div style="color: red; font-size: 30px">style binding1</div>
    <div :style="style1">style binding2</div>
    <button @click="style1.color = 'blue'">button</button>
  </div>
</template>
<script>
export default {
  components: {},
  data() {
    return {
      style1: {
        color: 'green',
        fontSize: '30px'
      }
    }
  },
  setup() {},
  created() {},
  mounted() {},
  unmounted() {},
  methods: {}
}
</script>
