<template>
  <div class="home">
    <h1 id="db">{{ message }}</h1>
    


    <h5>Who is the most intelligent?</h5>

    <div v-for="choice in choices" class="radio-inline">
    <input type="radio" v-bind:value="choice" v-on:click="add(choice)" name="optradio1">
    {{ choice }}
    </div>


      <h5>Who is the most powerful?</h5>

    <div v-for="choice in choices" class="radio-inline">
    <input type="radio" v-bind:value="choice" v-on:click="add(choice)" name="optradio2">
    {{ choice }}
    </div>


    <h5>Who is the most strongest?</h5>


    <div v-for="choice in choices" class="radio-inline">
    <input type="radio" v-bind:value="choice" v-on:click="add(choice)" name="optradio3">
    {{ choice }}
    </div>


    <h5>Who is the most Fastest man alive on Earth?</h5>


    <div v-for="choice in choices" class="radio-inline">
    <input type="radio" v-bind:value="choice" v-on:click="add(choice)" name="optradio4">
    {{ choice }}
    </div>


    <h5>Who is the most Fastest man alive in outerspace?</h5>


    <div v-for="choice in choices" class="radio-inline">
    <input type="radio" v-bind:value="choice" v-on:click="add(choice)" name="optradio5">
    {{ choice }}
    </div>


   
    <h5>Who can defy gravity?</h5>


    <div v-for="choice in choices" class="radio-inline">
    <input type="radio" v-bind:value="choice" v-on:click="add(choice)" name="optradio6">
    {{ choice }}
    </div>



     <button type="button" v-on:click="calc()" >Calculate</button>

     <div id="sup"></div>



  </div>
</template>

<style>
 
 #db{

    text-align: center;

 }

</style>

<script>
export default {
  data: function() {
    return {
      message: "Dg Questions",
      ans:"",
      choices: ["Bruce","Clark","Barry"],
      answer:[],
      zombie:[]

    };
  },
  created: function() {},
  methods: {

    add :function(input) {

      console.log(input);
      this.ans = input;
      console.log(this.ans);
      this.answer.push(input);
      console.log(this.answer);

    },


    calc :function() {
      
       document.getElementById("sup").innerHTML = ("Vishnu is a programmer");




    }


  },
  computed: {}
};
</script>