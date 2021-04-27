<template>
  <div id="plans">
    <div class="plan--container" :class="{active: isActive === 0}" @click="(e) => active(0)" >
      <div class="plan--icon-container">
        <StoreIcon class="plan--icon" alt="Store front" />
      </div>
      <div class="plan--text">
        <h1>Pro Plan</h1>
        <h2>Start now with the population</h2>
      </div>
      <span class="plan--price">
        $
        <span class="plan--price-number">300</span> 
        / year
      </span>
    </div>

    <div class="plan--container" :class="{active: isActive === 1}" @click="(e) => active(1)">
      <div class="plan--icon-container">
        <StoreIcon class="plan--icon" alt="Store front" />
      </div>
      <div class="plan--text">
        <h1>Medium Plan</h1>
        <h2>It's easy like one two three</h2>
      </div>
      <span class="plan--price">
        $
        <span class="plan--price-number">200</span> 
        / year
      </span>
    </div>

    <div class="plan--container" :class="{active: isActive == 2}" @click="(e) => active(2)">
      <div class="plan--icon-container">
        <StoreIcon class="plan--icon" alt="Store front" />
      </div>
      <div class="plan--text">
        <h1>Starter Plan</h1>
        <h2>Start now, don't hesitate</h2>
      </div>
      <span class="plan--price">
        $
        <span class="plan--price-number">100</span> 
        / year
      </span>
    </div>
  </div>
</template>

<script>
import StoreIcon from './svgs/StoreIcon.vue'

export default {
  name: 'Plans',
  data() {
    return { isActive: 0 }
  },
  components: { StoreIcon },
  methods: {
    active(value) {
      this.$data.isActive = value
    }
  }
}
</script>

<style>
  #plans {
    margin: 15px 0;
  }

  .plan--container {
    display: flex;
    flex-direction: row;
    justify-content: space-between;
    align-items: center;

    background-color: #f4f4f4;
    border-radius: 10px;
    border: solid 1px #e8e8e8;
    cursor: pointer;
    margin: 20px 0;
    padding: 10px;
  }

  .plan--container.active {
    background-color: #eafbf3;
    border: solid 1px #5fd69d;
  }

  .plan--container.active .plan--icon {
    fill: #58d599;
  }

  .plan--icon-container {
    display: flex;
    align-items: center;
    justify-content: center;

    border-radius: 100%;
    background-color: #fff;
    padding: 10px;
  }

  .plan--icon {
    height: 30px;
    fill: #d2d6df;
  }

  .plan--text h1 {
    font-size: 14px;
    margin: 0 !important;
  }

  .plan--text h2 {
    color: #999fa7;
    font-size: 12px;
    font-weight: 500;
  }

  .plan--price {
    display: flex;
    flex-direction: row;
    align-items: center;

    font-weight: 700;
  }

  .plan--price-number {
    font-size: 24px;
    font-weight: 600;
    margin: 0 5px;
  }
</style>
