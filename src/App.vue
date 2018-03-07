<template>
  <div>
    <img src="./assets/logo.png">
    {{mars}}
    <ul>
      <li v-for="(item,index) in list">{{item.name+"-"+item.price}}</li>
    </ul>
    <input type="text">
    <button v-on:click="addItem">addItem</button>
  </div>
</template>

<script>
export default {
  name: "App",
  data() {
    return {
      mars: "hehehehehehehe",
      list: [
        {
          name: "apple",
          price: 10
        },
        {
          name: "peal",
          price: 10
        }
      ]
    };
  },
  methods: {
    addItem() {
      console.log(this.list);  
    }
  }
};
</script>

<style>
#app {
  font-family: "Avenir", Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  margin-top: 60px;
}
</style>
