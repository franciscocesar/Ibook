<template>
  <div class="container-card">
    <h2 class="title">{{ typeCard }}</h2>
    <h1 class="preco"><small>$</small>{{ valueCard }}</h1>

    <div class="content-options">
      <hr />
      <p>{{ textCard }}</p>
      <hr />
      <p>{{ textCard }}</p>
      <hr />
      <p>{{ textCard }}</p>
      <hr />
    </div>
    <button class="container-button">LEARN MORE</button>
  </div>
</template>

<script lang="ts">
import Vue from 'vue'
export default Vue.extend({
  props: {
    typeCard: {
      type: String,
      default: '',
    },
    valueCard: {
      type: Number,
      default: 0,
    },
    textCard: {
      type: String,
      default: '1 TB Storage',
    },
  },
})
</script>

<style scoped>
.container-card {
  display: flex;
  flex-direction: column;
  align-items: center;
  background: rgb(8, 8, 73);
  background: linear-gradient(
    351deg,
    rgba(8, 8, 73, 1) 0%,
    rgba(149, 149, 150, 1) 0%,
    rgba(241, 241, 241, 1) 56%
  );
  box-shadow: rgba(0, 0, 0, 0.35) 0px 5px 15px;
  width: 20rem;
  height: 31rem;
  border-radius: 1rem;
  margin-top: 4rem;
  margin-left: 1.2rem;
}
.container-card h2 {
  color: rgb(83, 83, 83);
  font-size: 1.2rem;
  margin-top: 2.5rem;
}

.container-card:hover {
  background: rgb(8, 8, 73);
  background: linear-gradient(
    351deg,
    rgba(8, 8, 73, 1) 0%,
    rgba(2, 0, 36, 1) 0%,
    rgba(2, 31, 55, 1) 30%,
    rgba(16, 93, 129, 1) 90%
  );
}
.container-card:hover small,
.container-card:hover h2,
.container-card:hover h1,
.container-card:hover p {
  color: white;
}

.container-card h1 {
  font-size: 3.8rem;
  color: rgb(83, 83, 83);
}
.container-card h1 small {
  font-size: 2.1rem;
  color: rgb(83, 83, 83);
}
.content-options {
  margin-bottom: 1rem;
}
.content-options p {
  display: flex;
  justify-content: center;
  color: rgb(83, 83, 83);
  padding: 1.3rem;
  font-size: 1rem;
  font-weight: bold;
}
.container-button {
  font-weight: bold;
  letter-spacing: 1px;
  color: rgb(255, 255, 255);
  cursor: pointer;
  background-color: rgb(0, 0, 0);
  box-shadow: rgba(0, 0, 0, 0.35) 0px 5px 15px;
  width: 17rem;
  height: 2rem;
  border: solid 1.3px rgb(0, 0, 0);
  border-radius: 1vh;
  transition: transform 0.2s;
}
.container-button:hover {
  transform: scale(2);
}
hr {
  border: 1px solid rgba(255, 255, 255, 0.287);
  width: 200px;
}
</style>


