<template>{{ count }}</template>

<script lang="ts">
import { Vue, Options } from 'vue-class-component'

import { Emit } from 'vue-property-decorator'

// Component definition
@Options({
  // Define component options
  watch: {
    count: value => {
      console.log(value)
    }
  }
})
export default class Counter extends Vue {
  @Emit('test')
  test {
    return 'TEST'
  }

  // meta = setup(() => definePageMeta({ layout: 'admin' }))

  // The behavior in class is the same as the current
  count = 0

  increment() {
    this.count++
  }
}
</script>
