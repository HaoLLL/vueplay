<template>
<h1>This.vue</h1>
    
</template>
<script>
// 1. in method: this refers to the owner of the method(object)
// 2. function.call(object) apply() transfor this to person2
export default {
    data(){
        return {

        }
    },
    methods:{
        test(){
            var person = {
                firstName:"Lei",
                fullName:function(){
                    return this.firstName;
                }
            };
            var person1 = {
                fullName:function(){
                    return this.firstName + " "+ this.lastName;
                }
            }
            var person2 = {
               firstName:"Bill",
               lastName:"Gates",
            }
            
            console.log(person1.fullName.call(person2));
        }
    },
    created () {
        this.test();
        
    }
    
}
</script>
<style scoped>

</style>