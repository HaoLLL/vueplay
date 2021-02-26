<template>
    
</template>
<script>
// variable local/total
// f2可以访问n 返回f2 就可以在f1外面访问n f2 is closure
// n永远在内存中 
export default {
    created(){
        this.f();

    },
    methods:{
        f1(){
            var n =999;
            function f2(){
                n++;
                console.log(n);
            }
            return f2;
        },
        f(){
            var ff = this.f1();
            ff();
            ff();
        }
        
    }
    
}
</script>
<style scoped>

</style>