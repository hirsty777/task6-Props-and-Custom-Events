<template>
    <div class="userDataClass">
        <input class="input1" type="text" :value="inputUserName" @input="nameChange">
        <input class="input2" type="text" :value="inputUserAge" @input="ageChange"> 
    </div>
</template>





<script>
export default {
    emits:[
        'name-emit',
        'age-emit'
    ],
    data(){
        return{
            inputUserName:'',
            inputUserAge:'',
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