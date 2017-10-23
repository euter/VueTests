<template>
<div>
  <p>Test scoped slot</p>
  <ScopedSlotList 
    :items="items">
    <!-- scoped slot can be named too -->
    <li
      slot="item-idx"
      slot-scope="props">
      <span class="item ">{{props.index+1}}.</span>  
      {{ props.item.text }}
    </li>
  </ScopedSlotList>
</div>
</template>
<script>
import ScopedSlotList from './ScopedSlotList'

export default {
  name: 'ScopedSlotListUsage',
  data () {
    return {
      items: [{ text: 'sea' }, { text: 'fly' }, { text: 'air' }]
    }
  },
  components: {
    ScopedSlotList
  }
}
</script>
