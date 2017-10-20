<template>
    <ol>
    <slot name="item-idx"
        v-for="(item, index) in items"
        :item="item" :index="index">
        <!-- fallback content here -->
    </slot>
    </ol>
</template>
<script>
export default {
  name: 'AwesomeList',
  props: ['items']
}
</script>