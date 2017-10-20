<template>
<div>
  <p>Test scoped slot</p>
  <awesome-list :items="items">
    <!-- scoped slot can be named too -->
    <li
      slot="item-idx"
      slot-scope="props">
      {{props.index+1}}.  {{ props.item.text }}
    </li>
  </awesome-list>
</div>
</template>
<script>
import AwesomeList from './ScopedSlots'

export default {
  name: 'ListWithScopedSlot',
  data () {
    return {
      items: [{text: 'sea'}, {text: 'fly'}, {text: 'air'}]
    }
  },
  components: {
    AwesomeList
  }
}
</script>
