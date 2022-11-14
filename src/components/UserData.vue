<template>
    <input type="text" :value="inputUserName" @input="nameChange">
    <input type="text" :value="inputUserAge" @input="ageChange"> 
</template>





<script>
export default {
    data(){
        return{
            inputUserName:'name',
            inputUserAge:'age',
        }
    },
    methods:{
        nameChange(event){
            this.inputUserName=event.target.value;
            this.$emit('name-emit',this.inputUserName);
        },
        ageChange(event){
            this.inputUserAge=event.target.value;
            this.$emit('age-emit',this.inputUserAge);
        }
    }

}

</script>