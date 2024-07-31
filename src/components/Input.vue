<template>
  <input type="number" min="0" @input="changeAmount($event.target.value)" placeholder="Введите число">
  <button @click="convert()">Конвертация</button>
</template>

<script>
export default{
  props: {
    changeAmount: {
      type: Function,
      required: true,
    },
    convert: {
      type: Function,
      required: true
    }
  }
}
</script>

<style scoped>
input{
  outline: none;
  border-radius: 3px;
  border: 0;
  padding: 10px 15px;
  border-color: azure;
  color: #333;
  width: 500px;
  position: relative;
  top: -50px;
  font-size: 1.2em;
}

button{
  position: relative;
  top: -20px;
  padding: 15px 20px;
  color: #fff;
  text-transform: uppercase;
  cursor: pointer;
  background-color: #1a032d;
  outline: none;
  border: 0;
  border-radius: 3px;
}
</style>