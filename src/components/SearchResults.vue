<template>
  <div class="p-shadow-12 p-component result-item p-text-center">
    <router-link :to="{ name: 'Phrase', params: { id: datum.eid1 } }" tag="li" class="nounderline">
      <Button class="p-button-link">
        <span v-for="(v, k) in data.exprs[datum[datum.main]]" :key="k">
          {{data.tokens.values[data.tokens.keys.indexOf(v)].charAt(0)==='-'?'':'&nbsp;'}}{{ data.tokens.values[data.tokens.keys.indexOf(v)]}}
        </span>
    </Button>
    </router-link>
  </div>
</template>

<script>
export default {
  name: "SearchResults",
  props: {
    datum: Object,
    num: Number,
    data: Object
  }
}
</script>

<style scoped>
.result-item {
  padding: 1rem;
  margin: 2rem;
}
</style>
