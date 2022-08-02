<template>
  <div :="attributes">
    <h2> {{ firstName }} </h2>
    <a :href="link">{{ firstName }} {{source}}</a>
    <button @click="goNetlify">Mid Term Project</button>
    <input v-model="message" placeholder="Tu nombre es:">
    <p>Hola {{ message }}</p>
    <button @click="helloWorld">HelloWorld</button>
  </div>
</template>

<script>
export default {
  data(){
    return{
      firstName: "Marco Antonio",
      source:"GITHUB",
      link: "https://github.com/MarcoMorando",
      message:"",
      attributes:{
        id:"navBar",
        class:"flex-column"
      }
    };
  },
  methods:{
    goNetlify(){
      this.link = "https://marco-morando-mid-term-project.netlify.app/";
      this.source= "NETLIFY";
    },
    helloWorld(){
      console.log("Hello World");
      this.firstName="Hello World";
    }
  }
};
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>
h2 {
    color: #42b983;
    margin: 40px 0 0;
}

a{
  text-decoration: none;
}

.flex-column{
  display: flex;
  flex-direction: column;
  height: 300px;
  width: 100%;
  align-items: center;
  justify-content: space-between;
}
</style>