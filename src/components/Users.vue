<template>
    <div class="container">
        <Header/>
        <User/>
        <Button text='Generate'/>
    </div>
</template>

<script>

import Header from './Header.vue';
import User from './User.vue';
import Button from './Button.vue';

    export default {
    name: "Users",
    props: {},
    components: { 
        Button ,
        User,
        Header
    }
}
</script>