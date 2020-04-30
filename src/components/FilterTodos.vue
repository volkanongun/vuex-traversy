<template>
  <div>
    Filter Todos:
    <div class="select">
      <select @change="filterTodos($event)">
        <option value="200">200</option>
        <option value="100">100</option>
        <option value="50">50</option>
        <option value="20">20</option>
        <option value="10">10</option>
        <option value="5">5</option>
      </select>
    </div>
  </div>
</template>

<script>
import {mapActions} from 'vuex'

export default {

  name: 'FilterTodos',

  data () {
    return {

    }
  },

  methods: mapActions(['filterTodos'])
}
</script>

<style lang="css" scoped>
select {
  margin-top: 20px;
  padding: 6px;
  border: #41b883 1px solid;
  -webkit-appearance : none;
  -moz-appearance : none;
  appearance: none;
  outline: none;
  width: 10rem;
  cursor: pointer;
}
.select{
  display: inline-block;
  position: relative;
}
.select::after{
    content: "\25BC";
    position: absolute;
    color: white;
    background: #41b883;
    text-align: center;
    width: 14px;
    top: 20px;
    right: 0px;
    padding: 0rem 0.2rem 0.1rem 0.3rem;
    pointer-events: none;
}
</style>