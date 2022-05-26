<template>

<div class="reg-container">
    <img class="logo" src="../assets/logo.jpg" alt="logo.jpg" />
    <h1>Registration</h1>

    <div class="register">
        <input type="text" v-model="name" placeholder="Enter name" />
        <input type="text" v-model="email" placeholder="Enter email" />
        <input type="password" v-model="password" placeholder="Enter password" />
        <button class="btn" v-on:click="register">Signup</button>
    </div>

</div>

</template>


<script>
import axios from 'axios'
export default{
    name:'SignUp',
    data(){
        return {
            name:"",email:"",password:""
        }
    },
    methods:{
        async register(){
            let result = await axios.post('http://localhost:8000/user',{
                name:this.name,
                email:this.email,
                password:this.password
            })
            
            if(result.status == 201){
                alert("register done");
                localStorage.setItem("user-info",JSON.stringify(result.data))
            }
        }
    }
}
</script>


<style scoped>
.reg-container{
    /* height: 100vh;
    width: 100vh;
    margin-top: auto;
    margin-bottom: auto;
    margin: auto; */
}
h1{
    text-align:center;
}
img.logo {
    width: 100px;
    display: block;
    margin: 0 auto;
    background-color: red;
}
.register{
    width: 300px;
    margin:auto;
}
.register input{
    width:300px;
    display:block;
    padding:12px 12px;
    border:1px solid green;
    margin-bottom:10px;
}
.register .btn{
    width:324px;
    padding:14px 0px;
    background:green;
    border:none;
}
</style>


