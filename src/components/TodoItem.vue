<template>
    <div v-if="statuse==='Pending'||statuse=='Done'" 
    @mouseover="mouseOver()"
    @mouseleave="mouseLeave()"
    :class="status" @click="changeStatus">
        <h5 class="fw-bold text-start">{{task}}</h5>
        <my-button @click="deleteItem" deletes="DELETE" v-show="buttonVisible"/>
    </div>
</template>
<script>
import MyButton from './MyButton.vue';
export default {
  components: { MyButton },
    props:['status','task','id'],
    name:'TodoItem',
    data(){
        return{
            statuse:"",
            buttonVisible:false
        }
    },
    mounted(){
        this.statuse=this.status
    },
    emits:['change-status','onDelete-item'],
    methods:{
        changeStatus(){
            this.$emit("change-status");
        },
        mouseOver(){
            this.buttonVisible=true;
        },
        mouseLeave(){
            this.buttonVisible=false
        },
        deleteItem(){
            this.$emit('onDelete-item',this.id);
        }

    },

}
</script>
<style scoped>
    .Done{
        padding-top: 2%;
        padding-bottom: 1%;
        padding-left:2% ;
        padding-right:1% ;
        color: white;
        border: 3px solid black;
        background-color:#87CEEB;
        margin-top: 4%;
        display: flex;
        justify-content: space-between;
        align-items: center;
    }
    .Pending{
        padding-top: 2%;
        padding-bottom: 1%;
        padding-left:2% ;
        padding-right:1% ;
        border: 3px solid black;
        background-color:#C0C0C0;
        margin-top: 4%;
        display: flex;
        justify-content: space-between;
        align-items: center;
    }
</style>