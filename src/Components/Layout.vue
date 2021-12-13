<template>
   <div id="grid">
   <ServerList/>
   <ServerName/>
   <ChannelList/>
   <UserInfo/>
   <ChannelName/>
   <ChannelData/>
   </div>
</template>

<script>
import ServerList from "./ServerList";
import ServerName from "./ServerName";
import ChannelList from "./ChannelList";
import UserInfo from "./UserInfo";
import ChannelName from "./ChannelName";
import ChannelData from "./ChannelData";
export default{
    components:{
        ServerList,
        ServerName,
        ChannelList,
        UserInfo,
        ChannelName,
        ChannelData,
    }
}
</script>

<style scoped>
#grid{
    display: grid;
    height: 100vh;
    grid-template-columns: 71px 240px auto 240px;
    grid-template-rows: 40px auto 52px;
    grid-template-areas:
        "ServerList ServerName ChannelName ChannelName"
        "ServerList ChannelList ChannelData UserList"
        "ServerList UserInfo ChannelData UserList";
}
</style>
