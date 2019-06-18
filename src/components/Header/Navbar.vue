<template>
    <div>
      <div class="header">
        <ul>
          <li> {{ data.projeto }} </li>
          <li>{{ data.home }}</li>
          <li>{{ data.social }}</li>
        </ul>
      </div>
    </div>
</template>

<script>
/* eslint-disable */
export default {
  data(){
    return {
      data:{
        projeto: "</Project>",
        home: "</Home>",
        social: "</Social>",
      },
    }
  },
  methods: {

  },
}
</script>

<style scoped>
  .header{
    display: flex;
    flex: 1 1 1;
    width: 100%;
    flex-direction: row;
    flex-wrap: nowrap;
    justify-content: center;
    background-color: cornflowerblue;
    align-items: flex-start;
    align-content: flex-start;
  } 
  .header ul{
    display: flex;
    flex-direction: row;
    flex-wrap: nowrap;
    justify-content: space-between;
    align-items: flex-start;
    align-content: flex-start;
    width: 50%;
    align-self: stretch;
    /*background-color: #fff;*/
    padding:10px;
  }
  .header ul li{
    order: 0;
    flex-grow: 0;
    flex-shrink: 1;
    flex-basis: auto;
    list-style-type: none;
    align-self: stretch;
    padding: 5px;
    color: white;
    font-family: monospace;
    font-size: 15pt;
  }
  .header ul li:hover{
    transition: all .5s;
    background-color: cornflowerblue;
    color: white;
    cursor: pointer;
    text-shadow: 0.3px 0.3px 0.3px #fff;
  }
  .header ul li::selection{
    color: #1D1D1D;
  }
</style>
