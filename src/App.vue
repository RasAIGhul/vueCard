<template>
  <img alt="Vue logo" src="./assets/logo.png" />
  <HelloWorld msg="Hello Vue 3 + Vite" />
</template>

<script setup>
import HelloWorld from './components/HelloWorld.vue'

// This starter template is using Vue 3 experimental <script setup> SFCs
// Check out https://github.com/vuejs/rfcs/blob/script-setup-2/active-rfcs/0000-script-setup.md
</script>

<style>
.outsidediv{
    border: 8px solid #000;
    display: inline-block;
    vertical-align: middle;
    width: 400px;
  }
  .hingle {
    display: block;
    margin-left: auto;
    margin-right: auto;
    width: 400;
  }
  .titleCardHingle{
    text-align: center;
    font-family: "Copperplate",fantasy;
    font-size: 200%; 
    width: 400px;
    margin: auto;
  }
  .outside{
      text-align: center;
  } 
  .buttons button:hover,
  .buttons button:focus{
    background: red; 
  }
  .buttons{
    font-size: 20px;
    background: white;
  }
  
  @media (max-width: 600px) {
    .outsidediv {
      transform: scale(.9);
    }
  }
  
  .basic{
    background: orange;
  }
  
  .information{
    padding-inline-start: 0px;
    margin-block-end: 0em;
  }
  
  p{
      margin-block-end: 0;
  }

input:checked + label + .description { display:none; }



</style>
