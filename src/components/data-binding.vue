<template>
    <div class="div1">
      <input type="text" v-model="name">
      <h1 :style="{ textDecoration: decoration }">Hello {{name}} !</h1>
      <br>
      <a :href="link">Acesse o github</a>
    </div>
  </template>
  
  <script>
  export default{
    data: ()=> ({
      name: 'Miguel',
      link: 'https://github.com',
      decoration: 'underline'
    })
  }
  </script>
  
  <style>
  
  .div1{
    font-family: 'Segoe UI', Tahoma, Geneva, Verdana, bold
  }
  </style>
  
  