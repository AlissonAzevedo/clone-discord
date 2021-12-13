<template>
   <div class="container">
       <div class="messages">
           menssagens
       </div>

       <div class="input-text">
           <input type="text" placeholder="Conversar em #chat-adms">
           <div class="icon">
               <PlusCircle :size="24"/>
           </div>
       </div>
   </div>
</template>

<script>
import PlusCircle from "vue-material-design-icons/PlusCircle"
export default{
    components:{
        PlusCircle,
    }
}
</script>

<style lang="scss" scoped>
.container {
    grid-area: ChannelData;
    display: flex;
    flex-direction: column;
    justify-content: space-between;
    background-color: var(--primary);
    flex: 1;
}

.input-text{
    width: 100%;
    padding: 0 16px;
    height: 68px;
    input {
        width: 100%;
        height: 44px;
        padding: 0 10px 0 57px;
        border-radius: 7px;
        color: var(--white);
        background-color: var(--chat-input);
        position: relative;
        &::placeholder {
        color: var(--grey);
        }
    }
    .icon {
        color: var(--grey);
        position: relative;
        top: -50%;
        left: 14px;
        transition: ease-out all 0.2s;
        width: 24px;
        cursor: pointer;

        &:hover {
        color: var(--white);
        }
    }
}
</style>
