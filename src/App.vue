<template>
  <div class="wrapper">
    <div id="app">
      <NameForm />
    </div>
  </div>

  <footer>Made with ❤️ by <a href="https://github.com/azedeveloper">AzE</a> using <a href="https://genderize.io/">Genderize.io</a></footer>
  
</template>

<script>
import NameForm from './components/NameForm.vue';

export default {
  name: 'App',
  components: {
    NameForm
  }
};
</script>

<style>
  @import url('https://fonts.googleapis.com/css2?family=Poppins&display=swap');

  body {
    background-color: #141414;
    color: white;
    font-family: 'Poppins', sans-serif;
    overflow: hidden;
  }

  #app {
    margin-bottom: 50px;
  }

  .wrapper {
    position: absolute;
    top: 50%;
    left: 50%;
    transform: translate(-50%, -50%);
    align-items: center;
    justify-content: center;
    text-align: center;
  }

  input {
    background-color: #212121;
    border: #171717;
    font-size: 25px;
    font-variant-caps: all-petite-caps;
    color: white;
    outline: none;
    font-family: 'Poppins', sans-serif;
    border-radius: 12px;
  }

  button {
    margin-left: 10px;
    font-size: 20px;
    background-color: rgb(82, 82, 82);
    border: none;
    border-radius: 12px;
    color: white;
    width: 100px;
    cursor: pointer;
    height: 40px;
    font-family: 'Poppins', sans-serif;
  }

  #gender {
    font-size: 40px;
    margin-top: 40px;
  }

  footer {
    position: absolute;
    bottom: 0;
    width: 100%;
    height: 50px;
    align-items: center;
    justify-content: center;
    text-align: center;
  }

  a {
    color: white;
  }

  @media only screen and (max-width: 500px) {
    input {
      width: 300px;
      margin-bottom: 20px;
    }
  }

  @media only screen and (max-width: 350px) {
    input {
      width: 200px;
      font-size: 20px;
      margin-bottom: 20px;
    }
  }
</style>
