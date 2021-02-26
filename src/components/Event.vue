<template>
  <div>
    <input type="checkbox"
      v-bind:checked="checked"
      v-on:change="$emit('change',$event.target.checked)">
  </div>

</template>
<script>
export default {
    props:{
        checked:{
            type:Boolean,
            required:true,
            default:false
        }
    }
};
</script>
<style scoped>
</style>