<template>
  <q-select :value="value" color="secondary" @input="$emit('input', $event)" :options="items" filter clearable></q-select>
</template>

<script>
export default {
  name: 'ConfigItem',
  props: ['value'],
  data () {
    return {
      items: this.$store.state.items.items.map((item) => {
        return {
          value: item.name,
          label: item.name,
          sublabel: item.label,
          stamp: item.type
        }
      })
    }
  }
}
</script>
