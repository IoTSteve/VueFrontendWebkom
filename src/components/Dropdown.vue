<template>
  <div class="Dropdown">
    <select name="wochentage" id="wochentage">
    <option>Montag</option>
    <option>Dienstag</option>
    <option>Mittwoch</option>
    <option>Donnerstag</option>
    <option>Freitag</option>
  </select>
  

  </div>
</template>

<script>
export default {
  name: 'HelloWorld',
  props: {
    msg: String
  }
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>
</style>
