<template>
  <div id="container">
    <div>
      Wiadomości dnia: {{msg}}
      <br>
      Dziś jest {{today}}
      <br>
      Pogoda: {{weather}}
    </div>

    <div id="counter" v-bind:class="{ gtr: isGreater, lr: !isGreater}">{{count}}</div>
    <br>
    <button id="btn-counter" v-on:click="countUp">Count Up!</button>
  </div>
</template>

<script>
export default {
  name: "site",
  props: ["msg", "today", "weather"],
  data() {
    return {
      count: 0,
      isGreater: false
    };
  },
  methods: {
    countUp() {
      this.count++;
      this.isGreater = true;
    }
  }
};
</script>

<style scoped>
#container {
  font-size: 24px;
  color: black;
}

.gtr {
  background: #3ccf02;
  color: white;
}

.lr {
  background: rgba(30, 30, 30, 0.5);
}

#counter {
  font-size: 60px;
  border-radius: 20px;
  display: inline-block;
  line-height: 50px;
  padding: 20px;
  margin: 20px auto;
}

#btn-counter {
  width: 120px;
  height: 50px;
  border: none;
  cursor: pointer;
  font-size: 20px;
  border-radius: 20px;
  font-weight: bold;

  transition: all 0.3s;
  outline: 0;
}

#btn-counter:hover {
  background: gold;
}
</style>



