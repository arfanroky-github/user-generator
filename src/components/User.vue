<template>
    <div class="user" >
        <img :src="picture" :alt="firstName">
        <h2>{{firstName + ' ' + lastName}}</h2>
        <small>Email: {{email}}</small> <br> <br>
        <button style="outline: none; 
        border: none; 
        padding: .4rem .8rem; 
        background-color: green; 
        color: white;" 
        @click="getUser">
        Generate
      </button>

    </div>
</template>


<script>
    export default {
        name: 'User',
        data (){
            return {
            firstName: 'John',
            lastName: 'Doe',
            gender: 'male',
            email: 'john@gmail.com',
            picture: 'https://randomuser.me/api/portraits/men/10.jpg'
          }
        },
        methods: {
            async getUser(){

            const res = await fetch('https://randomuser.me/api');
            const {results} = await res.json();

            this.irstName= results[0].name.first,
            this.lastName= results[0].name.last,
            this.gender= results[0].gender,
            this.email= results[0].email,
            this.picture= results[0].picture.large
            }
        }

    }
</script>