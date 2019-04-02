<template>
    <div class="container">
      <div class="authentication-container">
        <div class="input-group">
          <label class="label">Username</label>
          <input type="text" v-model="username" class="input"  placeholder="Enter username">
        </div>
        <div class="input-group">
          <label class="label" >Password</label>
          <input type="password" class="input" v-model="password" placeholder="Enter password">
        </div>
       <button type="submit" class="buttonSubmit" @click="onSubmit">Log in</button>
      </div>
  </div>
</template>

<script>


export default {
  data: function () {
  return {
    password: '',
    username: ''
  }
  },
  methods: {
    onSubmit() {
      console.log("username:", this.username)
      console.log("password:", this.password)
    }
  }


}
</script>

<style>
.container {
    height: 95vh;
    position: relative;
    box-sizing: border-box;
   }

.authentication-container {
    background: #eeee;
    position: absolute;
    top: 50%;
    left: 50%;
    margin-right: -50%;
    transform: translate(-50%, -50%);
    text-align: center;
    border: 1px solid black;
    border-radius: 8px; }
    
.input-group {
   margin: 25px 50px;
}

.label {
  margin-right:30px;
  margin-top:5px;
  width:200px;
  font-size: 20px;
  text-align: left;
}
.input {
  width:300px;
  height: 40px;
  border-radius: 5px;
  padding-left: 5px;
}

.buttonSubmit {
  background-color: #ffff;
  margin-bottom: 30px;
  border-radius: 5px;
  border: solid 1px #8888;
  width:120px;
  height: 40px;
}
.buttonSubmit:hover {
  cursor: pointer;
}
</style>
