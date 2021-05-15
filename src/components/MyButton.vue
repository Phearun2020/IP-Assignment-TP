<template>
    <div>
        <button v-if="deletes=='DELETE'" class="btn delete"><em class="far fa-trash-alt"></em></button>
        
        <button v-if="add=='ADD'" class="btn plus"><em class="fas fa-plus"></em></button>
    </div>
</template>
<script>
export default {
    props:['deletes','add'],
    name:"MyButton",
    
}
</script>
<style scoped>
    .delete{
        padding-top: 20px;
        padding-bottom: 12px;
        padding-left: 30px ;
        padding-right: 30px ;
        margin-top: -18px;
        margin-bottom: -9px;
        margin-right: -10px;
        border: 3px solid black;
        background-color: red;
        color: white;
    }
    .delete:hover,.delete:focus{
        color: white;
        background-color: #b82309;
    }
    .plus{
        background-color: rgba(139, 33, 233, 0.788);
        color: white;
        border: 3px solid black;
        padding-top: 15px;
        padding-bottom: 15px;
        padding-left: 30px ;
        padding-right: 30px ;
    }
</style>