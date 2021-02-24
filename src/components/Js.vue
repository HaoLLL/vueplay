<template>
<h1>JS</h1>
<h1></h1>
    
</template>
<script>
// string number boolean null undefined
// var person = {}; new Object();
// .property / ["property"]
// for(var x in person){ console.log(person[x]); }
export default {
    methods:{
        change(){
            var person = {firstName:'Bill', lastName:'Gates'};
            for(var p in person){
                console.log(person[p]);
            }
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