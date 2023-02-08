<template>
  <h1>{{ msg }}</h1>

<!-- My custom code -->
  <div>
  <div class='buttons'>
    <button id="addToButton" class="buttons" v-on:click="duplicate"> Add Onto </button>
    <button id="deleteButton" class='buttons'> Delete Last</button>
    <button id="changeBackgroundButton" class='buttons' v-on:click="background"> Change Background</button>
    <button id="changeHeadingButton" class='buttons' v-on:click="heading"> Change Heading</button>
    <button data-toggle-button class = 'buttons'  v-on:click="toggleDetails"> Toggle Details </button>
  </div>
  
  <div class="outsidediv">
      <img class="hingle" src="https://pbs.twimg.com/profile_images/1288205058585300992/eH8L4MYG_400x400.jpg" />
      <div id='toChange'>
        <h1 class="titleCardHingle" id='title'> Hingle McCringleberry </h1>
        <div class="outside">
          <details class ='details'>
            <summary>Details</summary>
            <ul class="information">
              <p>Hingle McCringleberry is the 2012 Heisman-winning tight end out of Penn State University, selected No. 1 overall by the Rhinos in the 2016 NFL Draft.
              </p>
            </ul>
            </details>
        </div>
      </div>
  </div>
</div>
</template>

<script setup>
import { defineProps, reactive } from 'vue'

defineProps({
  msg: String
})

const state = reactive({ count: 0 })
</script>

<script>

export default {
  methods: {
    hoover() {
      document.querySelectorAll(".card").forEach((item) => {
        if(!item.classList.contains("hoverCard")){
          item.classList.add("hoverCard");
          console.log(item);
        }
        else{
          item.classList.remove("hoverCard");
          console.log(item);
        }
      });
    },
    
    duplicate() {
      const clone = document.querySelector('.outsidediv').cloneNode(true);
       document.body.appendChild(clone);   
    },

    background() {
        document.querySelectorAll('#toChange').forEach((item, index) => {
      if (!item.classList.contains('basic')) {
        item.classList.add('basic');
      }
      else {
        item.classList.remove('basic');
      }
    });
    },

    heading() {
      let name = prompt("Name Hingle");
      if(name){
        document.querySelector(".outsidediv #title").innerText = name;
    }
    },

    //Kinda borked rn
    deleter(){
      const elem = document.querySelector('.outsidediv:last-child');
      elem.remove();
    },

    toggleDetails(){
      if(details.parentNode.getAttribute('open'))
      { 
        details.parentNode.removeAttribute('open')
      }
    else{
      details.parentNode.setAttribute('open','open');
    }
      }
    },
};

</script>

<style scoped>
a {
  color: #42b983;
}
</style>
