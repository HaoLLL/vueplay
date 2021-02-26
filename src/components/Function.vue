<template>
    
</template>
<script>
// 函数声明
// 函数表达式
// Function() 构造器
// 自调用函数
// ES6 箭头函数 没有this 不适合定义对象方法
// call 将函数作用在不同的对象上面
// apply 接收数组形式的参数
export default {
    methods:{
        test(){
            return (function(){
                console.log("return function");
            })();
        },
        mockCall(){
            var person = {
                fullName:function(){
                    return this.firstName+" "+this.lastName;
                }
            }
            var person1 = {
                firstName:"Bill",
                lastName:"Gate",
            }
            console.log(person.fullName.call(person1));
        },
        mockApply(){
            var person = {
                fullName:function(city,country){
                    return this.firstName+" "+this.fullName+city+" "+country;
                }
            }
            var person1 = {
                firstName:"B",
                fullName:"G"
            }
            console.log(person.fullName.apply(person1,["SDFSDF","dfgs"]));
        }
        
        
    },
    created(){
        // this.test();
        this.mockApply();
    }
    
}
</script>
<style scoped>

</style>