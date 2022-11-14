<template>
    <active-user
        :name-active-prop="inputedName"
        :age-active-prop="inputedAge"
    ></active-user>


    <user-data
        @name-emit="getNameValue"
        @age-emit="getAgeValue"
    ></user-data>

</template>





<script>
export default {
    data(){
        return{
            inputedName:'Name',
            inputedAge:'Age'
        }
    },
    methods:{
        getNameValue(value){
            this.inputedName=value;
        },
        getAgeValue(value){
            this.inputedAge=value;
        }
    }
}
</script>




<style>


</style>