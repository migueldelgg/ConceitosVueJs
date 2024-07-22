<template>
    <div>
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
  </style>
  
  