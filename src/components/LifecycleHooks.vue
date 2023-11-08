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
    alert('beforeUpdate: We know an update is about to happen, and have the data')
  },
  updated() {
    alert('updated: virtual DOM will update after you click OK')
  },
  beforeCreate() {
    alert('beforeCreate: data is static, thats it')
  },
  created() {
    alert('created: data and events ready, but no DOM')
  },
  beforeMount() {
    alert('beforeMount: $el not ready')
  },
  mounted() {
    alert('mounted: DOM ready to use')
  },
  beforeUnmount() {
    alert('beforeUnmount: about to blow up this component')
  },
  unmounted() {
    alert('unmounted: this component has been destroyed')
  }
}
</script>

<style scoped>

</style>
