<template>
  <div class="search-bar">
      <select name="" id="" v-model="selectVal" @change="$emit('change',selectVal)">
          <option value="Rock">Rock</option>
          <option value="Pop">Pop</option>
          <option value="Jazz">Jazz</option>
          <option value="Metal">Metal</option>
      </select>
  </div>
</template>

<script>
export default {
    name: 'SearchBar',
        props: {
        info: Object
    },
    data() {
        return {
            selectVal: '',
        }
    },


}
</script>

<style lang='scss' scoped>

</style>