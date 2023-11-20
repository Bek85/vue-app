<template>
<div>
  <h1>Vue LifeCycle hooks</h1>
  <ul>
    <li v-for="(item, n) in list" :key="n">
      {{item}}
      <button @click="deleteItem(item)">Delete Item</button>
    </li>
  </ul>
</div>
</template>

<script>
export default {
  name: "LifecycleHooks",
  data() {
    return {
      list: [
          'Apex Legends',
          'A Plague Tale: Innocence',
          'ART SQOOL',
          'Baba Is You',
          'Devil May Cry 5',
          'The Division 2',
          'Hypnospace Outlaw',
          'Katana ZERO',
          'testing unmounted hooks'
      ]
    }
  },
  methods: {
    deleteItem(value) {
      this.list = this.list.filter(item => item !== value);
    }
  },
  beforeUpdate() {
    console.log('beforeUpdate: We know an update is about to happen, and have the data')
  },
  updated() {
    console.log('updated: virtual DOM will update after you click OK')
  },
  beforeCreate() {
    console.log('beforeCreate: data is static, thats it')
  },
  created() {
    console.log('created: data and events ready, but no DOM')
  },
  beforeMount() {
    console.log('beforeMount: $el not ready')
  },
  mounted() {
    console.log('mounted: DOM ready to use')
  },
  beforeUnmount() {
    console.log('beforeUnmount: about to blow up this component')
  },
  unmounted() {
    console.log('unmounted: this component has been destroyed')
  }
}
</script>

<style scoped>

</style>
