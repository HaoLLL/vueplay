<template>
    <button v-on:click="counter">You clicked me {{count}} times</button>
</template>
<script>
// data must be a function
// 
export default {
    data(){
        return  {
            count:0
        }
    },
    methods:{
        counter(){
            this.count++;
        }
    }
    
}
</script>
<style scoped>

</style>