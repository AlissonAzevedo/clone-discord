<template>
    <div class="container">
        <ServerButton isHome />
        <div class="separator">
        </div>
        <ServerButton :mentions="3"/>
        <ServerButton hasNotification />
        <ServerButton :mentions="999"/>
        <ServerButton/>
        <ServerButton hasNotification/>
        <ServerButton :mentions="134" hasNotification/>
        <ServerButton/>
        <ServerButton :mentions="455" hasNotification/>
        <ServerButton v-for=" servers in 12" :key="servers.id"/>
    </div>
</template>
<script>
import ServerButton from "./serverbutton";
export default{
    components:{
        ServerButton
    }
}
</script>

<style scoped lang="scss">
.container{
    grid-area: ServerList;
    display:flex;
    flex-direction:column;
    align-items:center;
    background-color: var(--tertiary);
    padding: 11px 0;
    max-height: 100vh;
    overflow-y: scroll;
    &::-webkit-scrollbar{
        display: none;
    }
}
.separator{
    width:32px;
    border-bottom:2px solid var(--quaternary);
    margin-bottom:8px;
}
</style>