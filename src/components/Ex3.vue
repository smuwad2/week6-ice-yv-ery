<script>
    export default { 

       // add code here
        data() {
            return {
                loginType: "username"
            };
        }
    }
</script>

<template>
    <h1>Please select your login option</h1>
    <!-- Add/modify code in the following to have a dropdown list 
        which lets the user to select either to login with username or email -->
    <select v-model="loginType">
        <option selected value="username">Username login</option>
        <option>Email login</option>
    </select>
    
    <div>
        <label v-if="loginType=='username'">Username</label>
        <label v-else>Email</label>
        <input v-if="loginType=='username'"placeholder="Enter your username">
        <input v-else placeholder="Enter your email address">
    </div>
</template>

