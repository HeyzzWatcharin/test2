<template>
  <!-- Default form login -->
  <div class="main">
    <form v-on:submit="login">
      <p class="h4 text-center mb-4">Sign in</p>
      <label for="defaultFormLoginEmailEx" class="grey-text">Your email</label>
      <input v-model="username" type="text" name="email" id="defaultFormLoginEmailEx" class="form-control"/>
      <br/>
      <label for="defaultFormLoginPasswordEx" class="grey-text">Your password</label>
      <input v-model="password" type="password" name="password" id="defaultFormLoginPasswordEx" class="form-control"/>
        <div class="text-center mt-4">
          
            <button class="btn btn-indigo" type="submit" value="Login">Login</button>
          
        </div>
    </form>
  </div>
  <!-- Default form login -->
</template>
<script>
  import { mdbInput, mdbBtn } from 'mdbvue';
  import axios from "axios"
  import router from '../routes/routes'
import Axios from 'axios';
  export default {
    name: 'Login',
    data :{
      username : '',
      password : ''
    },
    methods:{
      login: (e) => {    
        // e.preventDefault()   
        // let email = e.target.elements.email.value
        // let password = e.target.elements.password.value
        let login = () => {
          let data = {
            username: username,
            password: password
          }
          axios.post("api/login", data)
          .then((response) => {
            console.log("Logged in")
            router.push("/admin")
          })
          .catch((errors) => {
            console.log("Cannot login")
          })
        }
      login()      
    },
    components: {
      mdbInput,
      mdbBtn
    },
    }
  }
</script>

<style scoped>
  .main{
      margin-left: auto;
      margin-right: auto;
      margin-top: auto;
      max-width: 30%;
      position: relative;
      
  }
  .form-simple .font-small {
    font-size: 0.8rem; }

  .form-simple .header {
    border-top-left-radius: .3rem;
    border-top-right-radius: .3rem; }

  .form-simple input[type=text]:focus:not([readonly]) {
    border-bottom: 1px solid #ff3547;
    -webkit-box-shadow: 0 1px 0 0 #ff3547;
    box-shadow: 0 1px 0 0 #ff3547; }

  .form-simple input[type=text]:focus:not([readonly]) + label {
    color: #4f4f4f; }

  .form-simple input[type=password]:focus:not([readonly]) {
    border-bottom: 1px solid #ff3547;
    -webkit-box-shadow: 0 1px 0 0 #ff3547;
    box-shadow: 0 1px 0 0 #ff3547; }

  .form-simple input[type=password]:focus:not([readonly]) + label {
    color: #4f4f4f; }
</style>
