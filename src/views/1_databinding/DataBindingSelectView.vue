<template>
  <div>
    <div>
      <h1>select</h1>
      <select name="" id="" v-model="selectdCity">
        <option value=""></option>
        <option value="02">Seoul</option>
        <option value="031">Inchon</option>
      </select>
    </div>
    <div>
      <h1>combobox</h1>
      <div>
        <input
          type="checkbox"
          name=""
          id="html"
          value="HTML"
          v-model="favoriteLang"
        />
        <label for="HTML">HTML</label>
      </div>
      <div>
        <input
          type="checkbox"
          name=""
          id="css"
          value="CSS"
          v-model="favoriteLang"
        />
        <label for="CSS">CSS</label>
      </div>
      <div>
        <input
          type="checkbox"
          name=""
          id="js"
          value="JS"
          v-model="favoriteLang"
        />
        <label for="JS">JavaScript</label>
      </div>
      <div>select leg: {{ favoriteLang }}</div>
    </div>
    <div>
      <h1>radio</h1>
      <div>
        <input
          type="radio"
          name=""
          id="html"
          value="HTML"
          v-model="favoriteLang2"
        />
        <label for="HTML">HTML</label>
      </div>
      <div>
        <input
          type="radio"
          name=""
          id="css"
          value="CSS"
          v-model="favoriteLang2"
        />
        <label for="CSS">CSS</label>
      </div>
      <div>
        <input
          type="radio"
          name=""
          id="js"
          value="JS"
          v-model="favoriteLang2"
        />
        <label for="JS">JavaScript</label>
      </div>
      <div>select leg: {{ favoriteLang2 }}</div>
    </div>
  </div>
</template>
<script>
export default {
  components: {},
  data() {
    return {
      selectdCity: '02',
      favoriteLang: [],
      favoriteLang2: 'HTML'
    }
  },
  setup() {},
  created() {},
  mounted() {},
  unmounted() {},
  methods: {}
}
</script>
