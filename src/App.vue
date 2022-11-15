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
*{
    margin: 0;
    padding: 0;
    box-sizing: border-box;
}

#app{
    display: flex;
    flex-direction: row;
    text-align: center;
}

.activeUserClass{
    width: 50%;
    box-shadow: 0 4px 8px rgba(0, 0, 0, 0.671);
    border: 1px solid rgba(9, 9, 36, 0.5);
    padding: 40px ;
}
.userDataClass{
    display: flex;
    flex-direction: column;
    width: 50%;
    box-shadow: 0 4px 8px rgba(0, 0, 0, 0.671);
    border: 1px solid rgba(9, 9, 36, 0.5);
    padding: 40px ;
}

.input1, .input2{
    margin-left: 30%;
    max-width: 10rem;
}

</style>