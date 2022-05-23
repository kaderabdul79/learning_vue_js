<template>
    <img class="logo" src="../assets/logo.jpg" alt="logo.jpg" />
    <h1>Registration</h1>

    <div class="register">
        <input type="text" placeholder="Enter name" />
        <input type="text" placeholder="Enter email" />
        <input type="password" placeholder="Enter password" />
        <button class="btn">Signup</button>
    
    </div>


</template>


<script>
export default{
    name:'SignUp'
}
</script>


<style scoped>
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
    width: 250px;
    margin:0 auto;
}
.register input{
    width:200px;
    display:block;
    padding:8px 12px;
    border:1px solid green;
    margin-bottom:10px;
}
.register .btn{
    width:224px;
    padding:14px 0px;
    background:green;
    border:none;
}
</style>


