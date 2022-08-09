<template>
  <h3>TTER</h3>
  <Icon Icon="bi:person-square" />
  <div class="container">
    <div class="input">
      <div class="in">
        <span class="dollar">$ </span><input type="number" />
      </div>
      <div class="button">
        <button>5%</button>
        <button>10%</button>
        <button>15%</button>
        <button>25%</button>
        <button>50%</button>
        <button class="custom">custom</button>
      </div>
      <div class="in">
        <input type="number" />
      </div>
    </div>
    <div class="output">
      <div class="calculator">
        <div class="tip-amount">
          <div class="person">
            <span>Tip Amount</span>
            <span class="regular">/ person</span>
          </div>
          <div class="price">$ 0.00</div>
        </div>
        <div class="total-tip">
          <div class="person">
            <span>Total</span>
            <span class="regular">/ person</span>
          </div>
          <Icon icon="bi:person" />
          <div class="price">$ 0.00</div>
        </div>
      </div>
      <div>
        <div class="reset"><button>RESET</button></div>
      </div>
    </div>
  </div>
</template>
<script>
import { Icon } from "@iconify/vue";
export default {
  Components: {
    Icon,
  },
};
</script>
<style>
* {
  margin: 0;
  padding: 0;
}
body {
  background-color: aqua;
}
#app {
  height: 100vh;
  display: flex;
  flex-direction: column;
  row-gap: 30px;
  justify-content: center;
  align-items: center;
}

.container {
  margin: 20px;
  background-color: white;
  width: 1200px;
  height: 600px;
  display: flex;
  align-items: center;
  border-radius: 16px;
}
.input,
.output {
  width: 50%;
  height: 90%;
  margin: 25px;
}
.input {
  display: flex;
  flex-direction: column;
  row-gap: 120px;
}

.output {
  background-color: rgb(10 64 57);
  display: flex;
  flex-direction: column;
  justify-content: space-between;
  border-radius: 12px;
}
.input div {
  height: 8%;
  display: flex;
  align-items: center;
}
.input .dollar {
  position: relative;
  left: 12px;
}

.input input {
  margin: 0 18px;
  margin-right: 5px;
  width: 95%;
  height: 40px;
  border: none;
  outline: none;
  background-color: rgb(206, 243, 231);
  text-align: right;
  font-size: 18px;
  font-family: Cambria, Cochin, Georgia, Times, "Times New Roman", serif;
}
.input .in {
  border: 1px solid black;
  background-color: rgb(206, 243, 231);
}
Icon {
  height: 30px;
  width: 30px;
  z-index: 2;
}
.input button {
  width: 28%;
  height: 23%;
  background-color: rgb(10 64 57);
  color: white;
  font-size: 20px;
}
.input button:focus {
  background-color: rgb(24, 198, 137);
}
.input .button {
  height: 40%;
  display: flex;
  flex-wrap: wrap;
  column-gap: 30px;
  justify-content: center;
}
.input .custom {
  color: black;
  background-color: white;
}
.calculator {
  font-family: Arial, Helvetica, sans-serif;
  height: 30%;
  display: flex;
  flex-direction: column;
  justify-content: space-between;
  margin-top: 20px;
}
icon {
  color: black;
}
.tip-amount,
.total-tip {
  display: flex;
  justify-content: space-between;
  margin: 20px;
}
.person {
  display: flex;
  flex-direction: column;
  color: white;
}
.regular {
  font-weight: 200;
  font-size: small;
}
.price {
  color: rgb(3, 145, 93);
  font-size: 40px;
  font-weight: 700;
}

.output .reset {
  display: flex;
  justify-content: center;
  width: 100%;
  height: 50px;
  margin-bottom: 20px;
}
.output button {
  width: 90%;
  height: 45px;
  background-color: rgb(24, 198, 137);
  border: none;
  border-radius: 5px;
}
</style>