<template>
<h1>JS</h1>
<h1></h1>
    
</template>
<script>
// string number boolean null undefined
// var person = {}; new Object();
// 
export default {
    methods:{
        change(){
            var person = {firstName:'Bill'};
            var x = person;
            x.firstName = "bbb";
            alert(x.firstName);
        }  
    },
    created(){
        this.change();
    },
    data(){
        return  {
            
        }
    }

}
</script>
<style scoped>

</style>