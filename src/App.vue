<template>
 <!--<h2 v-bind:innerHTML="val" v-bind:class="className"></h2>
  <button v-on:click="testing('My Message')">Click Me </button>
  <button v-on:click="changeColor">{{ btnText }}</button>
  <ul>
    <li v-for="emp in employees" v-bind:key="emp.id"> {{ emp.name }}</li>
  </ul> -->

<div>

<Contact name='Nidhi' />

<Contact name='Neha' email='user@gmail.com'/>

<Contact  email='user@gmail.com' contacted='1' />
</div>

</template>

<script>

import Contact from './components/contact.vue';
export default {
  name: 'App',
  components: {
    Contact
  },

  data(){
    return {
      val: 'This is the default value',
      className: 'blueText',
      btnText: 'Change to red',

      employees: [
      
        {
          id: 101,
          name:'Nidhi'
        },

        {
          id: 102,
          name:'Shalu'
        },

        {
          id: 103,
          name:'Ankita'
        },

        {
          id: 104,
          name:'Viki'
        },

      ]
    
    }
  },



  
  methods: {
    testing: function(val){
      alert(val);
    },

    changeColor: function(){


     console.log(this.className);

     this.btnText = this.btnText == 'Change to red' ? 'Change to blue' : 'Change to red' ;

      if(this.className=="blueText")
        this.className="redText"
      else
        this.className="blueText";
    }
  },


}
</script>

<style scoped>

.blueText{
  color:blue;
  background-color: lightcyan;
}


.redText{
  color:red;
  background-color: lightcyan;
}
<style>
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  margin-top: 60px;
}
</style>
