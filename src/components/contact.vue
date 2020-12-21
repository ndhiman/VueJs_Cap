<template>
 <div v-bind:style = "contacted ? 'background-color: coral': 'background-color: active'" class='box'>

 <h3 v-if='name'> {{ name }} </h3>
 <h3 v-else> No name </h3>

 <hr>

 <h4> Email: {{ email }} </h4>
 <h4 v-if='mobile'> {{ mobile }} </h4>

 </div>
</template>

<script>

  export default {
      name: 'Contact',
      props: {

          name:String,
          email:String,
          mobile:String,
          contacted:Boolean

      }
  }

  </script>


  <style scoped>

     .box{

         background-color : lightcyan;
         color: blue;
         border: 2px solid blue;
         padding: 10px;
         margin: 10px;
         display: inline-block;
         border-radius: 20px;
     }
  </style>