<template>
    <div>
      <div class="header">
        <ul>
          <li>Item 01</li>
          <li>Item 01</li>
          <li>Item 01</li>
        </ul>
      </div>
    </div>
</template>

<script>
/* eslint-disable */
export default {
  data(){
    return {
      data:'',
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
    background-color: #333;
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
    background-color: #fff;
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
  }
  .header ul li:hover{
    transition: all .5s;
    background-color: cornflowerblue;
    color: white;
    cursor: pointer;
  }
</style>
