<template>
  <div class="container">
    <Header />
    <div class="bloco">
      <input
        type="radio"
        id="botao01"
        name="toggle_option"
        @click="show = !show"
        checked
      />
      <input
        type="radio"
        id="botao02"
        name="toggle_option"
        @click="show = !show"
      />

      <label class="button-cont" for="botao01"><span>Mensal</span></label>
      <label class="button-cont" for="botao02"><span>Anual</span></label>
      <div class="botao_slider"></div>
    </div>

    <transition 
        enter-active-class="animate__animated animate__backInLeft"
        
           
    >
        <div class="container-agroup" v-if="show">
        <Card typeCard="Basic" valueCard=10.00 />
        <CardHome typeCard="Professional" valueCard=15.00 />
        <Card typeCard="Master" valueCard=18.00 />
        </div>
     </transition>

    <transition  enter-active-class="animate__animated animate__backInLeft"
    >
        <div class="container-agroup" v-if="!show">
            <Card typeCard="Basic" valueCard=22.99 />
            <CardHome typeCard="Professional" valueCard=30.00 />
            <Card typeCard="Master" valueCard=45.00 />
        </div>
    </transition>
  </div>
</template>

<script lang="ts">
import Vue from 'vue'
import 'animate.css'
export default Vue.extend({
  data() {
    return {
      show: false,
    }
  },
})
</script>

<style>
.container {
  display: flex;
  justify-content: center;
  align-items: center;
  flex-direction: column;
}
.container-agroup {
  display: flex;
}

.bloco {
  display: table;
  position: relative;
  width: 170px;
  padding: 5px 10px;
  background: linear-gradient(
    351deg,
    rgba(8, 8, 73, 1) 0%,
    rgba(149, 149, 150, 1) 0%,
    rgba(241, 241, 241, 1) 56%
  );
  box-shadow: rgba(0, 0, 0, 0.24) 0px 3px 8px;
  margin: 50px auto;
  -webkit-border-radius: 50px;
  -moz-border-radius: 50px;
  border-radius: 50px;
}
.bloco input[type='radio'] {
  display: none;
}
.bloco label {
  float: left;
  font-family: 'Source Sans Pro';
  font-size: 16px;
  width: calc(100% / 3);
  padding: 10px;
  color: #fff;
  -webkit-border-radius: 50px;
  border-radius: 50px;
  cursor: pointer;
  text-align: center;
}
/*O SLIDE QUE VAI DESLIZAR ATÉ O BOTÃO CLICADO*/
.botao_slider {
  position: absolute;
  background: rgba(1, 0, 3, 0.541);
  top: 13px;
  width: 50px;
  height: 25px;
  padding: 0 10px;
  -webkit-border-radius: 50px;
  -moz-border-radius: 50px;
  border-radius: 50px;
  -webkit-transition: all 0.5s ease;
  transition: all 0.5s ease;
}

#botao01:checked ~ .botao_slider {
  left: 15px;
}
#botao02:checked ~ .botao_slider {
  left: 94px;
}
.button-cont span {
  font-family: 'Lato';
  font-size: 1.4vh;
  font-weight: bold;
  color: rgb(1, 0, 7);
}
</style>
