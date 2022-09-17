<template>
    <div class="container">
        <Header/>
        <User />

    </div>
</template>

<script>

import Header from './Header.vue';
import User from './User.vue';


    export default {
    name: "Users",
    props: {
       
    },
    components: { 
        User,
        Header
    }
}
</script>