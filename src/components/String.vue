<template>
    
</template>
<script>
export default {
    methods:{
        test(){
            var txt = "ABCDEFGHIJKLMN";
            var sin = txt.length;
            console.log(sin);
            console.log(txt.indexOf("A"));
            console.log(txt.search("A"));
            console.log(txt.slice(-1));
            console.log(txt.substring(0,1));// do not accept -1
            console.log(txt.substr(0,2)); // length
            var newS = txt.replace("A","a");
            console.log(newS);
            console.log(txt.toUpperCase());
            console.log(txt.toLowerCase());
            console.log(txt.concat("KKKKKK"));
            console.log(txt.charAt(0));
            console.log(txt.split(","));
        }
    },
    created(){
        this.test();
    }
    
}
</script>