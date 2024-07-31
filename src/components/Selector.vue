<template>
  <ul>
    <li @click="selectItem('BTC')" :class="current == 'BTC' ? 'active' : ''">
      Bitcoin
    </li>
    <li @click="selectItem('ETH')" :class="current == 'ETH' ? 'active' : ''">
      ETH
    </li>
    <li @click="selectItem('USDT')" :class="current == 'USDT' ? 'active' : ''">
      USDT
    </li>
  </ul>
</template>

<script>
export default {
  props: {
    setCrypto: {
      type: Function,
      required: true,
    },
  },
  data() {
    return {
      current: "",
    };
  },
  methods: {
    selectItem(val) {
      this.setCrypto(val);
      this.current = val;
    },
  },
};
</script>

<style scoped>
ul {
  list-style: none;
  width: 200px;
  padding: 0;
  margin: 0 auto;
  border-radius: 3px;
  border: 3px solid;
}

li {
  display: block;
  background: rgb(2, 0, 36);
  background: linear-gradient(
    90deg,
    rgba(2, 0, 36, 1) 0%,
    rgba(0, 212, 255, 1) 0%,
    rgba(9, 119, 121, 0.3881885517879027) 56%,
    rgba(225, 42, 148, 1) 100%
  );
  color: #fff;
  padding: 20px 0;
}

li:hover,
li.active {
  background: #24043e;
  cursor: pointer;
}
</style>
