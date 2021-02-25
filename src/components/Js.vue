<template>
<h1>JS</h1>
<h1></h1>
    
</template>
<script> 
// var person = {}; new Object();
// .property / ["property"]
// for(var x in person){ console.log(person[x]); }
// var x = 911+"Porsche" = "911"+"Porsche"
// var x; undefined
// typeof "Bill" typeof array = object typeof null = object
// typeof undefined = undefined
// null to be used to clear the object value
// === to justify the type    ==  to justify the value
// 原始数据 string number boolean undefined null symbol(es6)
// 复杂数据 function object array
// javascript = ECMAScript + DOM + BOM
// type object array null = object
export default {
    methods:{
        change(){
            var person = {firstName:'Bill', lastName:'Gates'};
            for(var p in person){
                // console.log(person[p]);
            }
            var x = {
                callName:function(){
                    return  "asdf";
                }
            }
            console.log(x.callName());
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