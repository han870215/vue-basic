<template>
  <div>
    <div>
      <select name="" id="">
        <option value=""></option>
        <option value="" :key="city.code" v-for="city in cities">
          {{ city.title }}
        </option>
      </select>
    </div>
    <div>
      <table>
        <thead>
          <tr>
            <th>id</th>
            <th>name</th>
            <th>price</th>
            <th>qty</th>
            <th>sum</th>
          </tr>
        </thead>
        <tbody>
          <tr :key="drink.id" v-for="drink in drinkList">
            <td>{{ drink.id }}</td>
            <td>{{ drink.name }}</td>
            <td>{{ drink.price }}</td>
            <td><input type="number" name="" id="" v-model="drink.qty" /></td>
            <td>{{ drink.price * drink.qty }}</td>
          </tr>
        </tbody>
      </table>
    </div>
  </div>
</template>
<script>
export default {
  components: {},
  data() {
    return {
      cities: [
        { title: 'seoul', code: '02' },
        { title: 'busan', code: '051' },
        { title: 'jeju', code: '064' }
      ],
      drinkList: [
        {
          id: '1',
          name: 'coke',
          price: 700,
          qty: 1
        },
        {
          id: '2',
          name: 'orange',
          price: 1200,
          qty: 1
        }
      ]
    }
  },
  setup() {},
  created() {},
  mounted() {},
  unmounted() {},
  methods: {}
}
</script>
