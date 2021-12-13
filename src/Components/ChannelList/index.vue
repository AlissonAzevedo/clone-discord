<template>
   <div class="container">
       <div class="category">
           <div>Canais de Texto</div>
           <div class="category-icon">
               <AddCategoryIcon :size="20"/>
           </div>
       </div>
       <ChannelButton channelName="chat-geral"/>
       <ChannelButton selected channelName="chat-adms"/>
       <ChannelButton channelName="chat-csgo"/>
       <ChannelButton channelName="chat-valorant"/>
       <ChannelButton channelName="chat-AFK"/>
   </div>
</template>

<script>

import AddCategoryIcon from "vue-material-design-icons/Plus";
import ChannelButton from "./ChannelButton";

export default{
    components:{
        AddCategoryIcon,
        ChannelButton    
    }
    
}  
</script>

<style lang="scss" scoped>
.container{
    grid-area: ChannelList;
    display: flex;
    flex-direction: column;
    padding: 24px 10px 0 16px;
    background-color: var(--secondary)
}
.category{
    display: flex;
    align-items: center;
    justify-content:space-between;
    margin-bottom:6px;
    color: var(--grey);
    font-size: 12px;
    font-weight: 500;
    text-transform: uppercase;
    transition: all ease-out 0.2s;
    cursor: pointer;

    .category-icon{
        color: var(--symbol);
        cursor: pointer;
        transition: all ease-out 0.2s;
        &.active,
        &:hover {
            color: var(--white);
        }
        
    }
    &.active,
    &:hover {
        color: var(--white);
    }
}
</style>