<template>
  <div class="home">
    <form @submit.prevent="sendData">
      <div class="form-control">
        <label for="name">Name</label>
        <input v-model="name" id="name" type="text">
      </div>
      <div class="form-control">
        <label for="email">Email</label>
        <input v-model="email" id="email" type="email">
      </div>
      <div class="form-control">
        <label for="address">Address</label>
        <input v-model="address" id="address" type="text">
      </div>
      <div class="form-control">
        <label for="gender">Gender</label>
        <input v-model="gender" id="gender" type="radio" value="male">
        <input v-model="gender" id="gender" type="radio" value="female">
      </div>
      <input type="submit" class="send" value="Send">
    </form>
  </div>
</template>

<script>
// @ is an alias to /src

export default {
  name: 'home',
  data: function () {
    return {
      name: '',
      email: '',
      address: '',
      gender: '',
    }
  },
  methods: {
    sendData() {
      console.log(this.name);
    }
  }
}
</script>

<style>
  .form-control {
    padding: 5px;
  } 

  .form-control label {
    display: block;
  }

  .send {
    margin: 5px
  }
</style>