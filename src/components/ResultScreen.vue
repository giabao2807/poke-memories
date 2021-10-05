<template>
  <div class="screen">
    <h1>✨ Congratulations ✨</h1>
    <h2>🍓🍓🍓🍓🍓🍓🍓🍓🍓🍓🍓🍓</h2>
    <h3>{{ Math.round(timer / 920) }} seconds</h3>
    <button @click="onStartAgain">Start Again</button>
    <br>
    <br>
    <div align="center">
    <h5 >Connect with me</h5>
    <p>
      <a href = "https://www.facebook.com/giabaobao2807/"><img src="https://img.icons8.com/color/48/000000/facebook.png"/></a>
      <a href = "https://twitter.com/giabao2807"><img src="https://img.icons8.com/fluent/48/000000/twitter.png"/></a>
      <a href = "https://www.instagram.com/giabao.izhere/"><img src="https://img.icons8.com/fluent/48/000000/instagram-new.png"/></a>
      <a href= "mailto:dinhgiabao2807@gmail.com"><img src="https://img.icons8.com/fluency/48/000000/gmail-new.png"/></a>
      <a href = "https://www.youtube.com/channel/UCBImcNeAi4soXFwQnACdkXA"><img src="https://img.icons8.com/color/48/000000/youtube-play.png"/></a>
    </p>
    </div>
    
  </div>
</template>

<script>
export default {
  props: {
    timer: {
      type: Number,
      default: 0,
    },
  },
  emits: ["onStartAgain"],
  methods: {
    onStartAgain() {
      this.$emit("onStartAgain");
    },
  },
};
</script>

<style scoped>
.screen {
  width: 100%;
  height: 100vh;
  position: absolute;
  top: 0;
  left: 0;
  z-index: 2;
  background-color: var(--dark);
  color: var(--light);
  display: flex;
  align-items: center;
  justify-content: center;
  flex-direction: column;
}

.screen h1 {
  font-size: 5rem;
}

.screen h3 {
  margin-top: 1.5rem;
  font-size: 3rem;
}

.screen button {
  font: var(--font);
  background: transparent;
  box-shadow: none;
  border: 1px solid var(--light);
  color: var(--light);
  margin: 1rem;
  padding: 1rem 1.25rem;
  border-radius: 0.5rem;
  font-size: 1.25rem;
  cursor: pointer;
  transition: background 0.3s ease-in-out;
}

.screen button:hover {
  background-color: var(--light);
  color: var(--dark);
}
</style>
