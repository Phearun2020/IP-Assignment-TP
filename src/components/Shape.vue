<template>
    <heart v-if="name=='Heart'" :color="color"></heart>
    <star v-else-if="name=='Star'" :color="color"></star>
    <traingle v-else-if="name=='Traingle'" :color="color"></traingle>
    <hexagone v-else-if="name=='Hexagone'" :color="color"></hexagone>
    <diamond v-else-if="name=='Diamond'" :color="color"></diamond>

    
</template>

<script>
export default {
    name: 'Shaped',
    props: ['name','color'],
}
</script>