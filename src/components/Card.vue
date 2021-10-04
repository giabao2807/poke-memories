<template>
  <div class="card">
    <div class="card__inner">
      <div class="card__face card__face--font">
        <div class="card_content">Font</div>
      </div>
      <div class="card__face card__face--back">
        <div class="card_content">Back</div>
      </div>
    </div>
  </div>
</template>

<style lang="css" scoped>
  .card{
    display:inline-block;
    margin-right:1rem;
    margin-bottom:1rem;
  }

  .card__inner{
    width:100%;
    height:100%;
    transition: transform 1s;
    cursor: pointer;
    position: relative;
  }

  .card__inner.is-flipped{
  }
</style>
