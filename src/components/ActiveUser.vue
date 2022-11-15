<template>
    <div class="activeUserClass">
        <h2>Name:{{ nameActiveProp }}</h2>
        <h3>Age:{{ ageActiveProp }}</h3> 
    </div>
   
</template>





<script>
export default {
    props:[
        'nameActiveProp',
        'ageActiveProp'
    ]
}

</script>