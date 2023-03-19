<template>
  <div>
    <img src="../assets/logo.png" alt="Logo" id="logo">
    <h1>What gender is your name?</h1>
    <input v-model="name" type="text" placeholder="name">
    <button @click="submitName">Go!</button>
    <div v-if="gender" id="gender">{{ gender }}</div>
  </div>
</template>

<script>
import axios from 'axios';

export default {
  name: 'NameForm',
  data() {
    return {
      name: '',
      gender: null
    };
  },
  methods: {
    async submitName() {
      if (!this.name) {
        return this.gender = "❌ You have to enter a name!";
      }
      const response = await axios.get(`https://api.genderize.io?name=${this.name}`);
      this.gender = response.data.gender === 'male' ? '♂️ Male' : '♀️ Female';
    }
  }
};
</script>

