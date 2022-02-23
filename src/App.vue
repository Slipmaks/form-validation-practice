<template>
  <div class="container">
    <div class="wrap">
      <div class="header">
        <h2>Посчитать прибыль</h2>
        <p>Добриво</p>
      </div>
      <form class="form" id="form">
        <div class="form-control">
          <label>Урожайность</label>
          <input
            type="text"
            placeholder="20"
            v-model="productivity"
            @mouseleave="addClass"
          />
          <small>Error message</small>
        </div>
        <div class="form-control">
          <label>Стоимость хим удобрения</label>
          <input type="text" placeholder="3000" v-model="price" />
          <small>Error message</small>
        </div>
      </form>
    </div>
  </div>
</template>
<script>
import { ref } from "vue";

export default {
  setup() {
    const productivity = ref("");
    const price = ref("");
    return { productivity, price };
  },
};
</script>
<style>
* {
  box-sizing: border-box;
}
body {
  display: flex;
  align-items: center;
  justify-content: center;
  min-height: 100vh;
  margin: 0;
}
.container {
  background-color: #e9e5e4;
}
.wrap {
  display: inline-block;
  margin: 10px 10px;
  background-color: #f2f1ef;
  border: 1px dashed;
}
.form-control {
  margin: 0px 20px 10px 20px;
  padding-bottom: 10px;
  position: relative;
}
.header {
  text-align: center;
  margin: 10px;
}
.form-control input {
  border: 1px solid #dbdddd;
  margin-top: 10px;
  padding: 10px;
  font-size: 14px;
  display: block;
  width: 100%;
  border-radius: 3px;
}
.form-control input:focus-visible {
  outline: 1px solid #dbdddd;
}
.form-control.error input {
  border-color: #e74c3c;
}
.form-control small {
  visibility: hidden;
  position: absolute;
}
</style>
