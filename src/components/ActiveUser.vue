<template>
    <h2>Name:{{ nameActiveProp }}</h2>
    <h3>Age:{{ ageActiveProp }}</h3>
</template>





<script>
export default {
    props:[
        'nameActiveProp',
        'ageActiveProp'
    ]
}

</script>