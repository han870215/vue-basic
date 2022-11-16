<template>
  <div>
    <select @change="changeCity($event)" v-model="selectedCity">
      <option value="">==city select==</option>
      <option
        :key="city.cityCode"
        :value="city.cityCode"
        v-for="city in cityList"
      >
        {{ city.title }}
      </option>
    </select>
    <!-- <select name="" id="">
      <option
        :key="dong.dongCode"
        :value="dong.dongCode"
        v-for="dong in dongList.filter(
          (dong) => dong.cityCode === selectedCity
        )"
      >
        {{ dong.dongTitle }}
      </option>
    </select> -->
    <select name="" id="">
      <option
        :key="dong.dongCode"
        :value="dong.dongCode"
        v-for="dong in selectedDongList"
      >
        {{ dong.dongTitle }}
      </option>
    </select>
  </div>
</template>
<script>
export default {
  components: {},
  data() {
    return {
      selectedCity: '',
      cityList: [
        { cityCode: '02', title: 'seoul' },
        { cityCode: '051', title: 'jeju' }
      ],
      dongList: [
        { cityCode: '02', dongCode: '1', dongTitle: 'seoul 1dong' },
        { cityCode: '02', dongCode: '2', dongTitle: 'seoul 2dong' },
        { cityCode: '02', dongCode: '3', dongTitle: 'seoul 3dong' },
        { cityCode: '051', dongCode: '1', dongTitle: 'jeju 1dong' },
        { cityCode: '051', dongCode: '2', dongTitle: 'jeju 2dong' }
      ],
      selectedDongList: []
    }
  },
  setup() {},
  created() {},
  mounted() {},
  unmounted() {},
  methods: {
    changeCity(event) {
      console.log(event.target.tagName)
      this.selectedDongList = this.dongList.filter(
        (dong) => dong.cityCode === this.selectedCity
      )
    }
  }
}
</script>
