<template>
  <div id="about">
    <div class="about--top">
      <div class="about--icon-container">
        <PersonIcon class="about--icon" alt="Generic siloutte of person icon" />
      </div>
      <div class="about--text">
        <h1>Tell us about you</h1>
        <h4>Some basic details to get started</h4>
      </div>
      <div class="about--close-button"></div>
    </div>
    <div class="about--inputs">
      <input type="email" placeholder="Email" class="about--inputs-email" />
      <div class="about--inputs-names">
        <input type="text" placeholder="First Name" class="about--inputs-first" />
        <input type="text" placeholder="Last Name" class="about--inputs-last" />
      </div>
    </div>
    <button class="about--button" type="submit">Sign Up</button>
  </div>
</template>

<script>
import PersonIcon from './svgs/PersonIcon.vue'
export default {
  name: 'About',
  components: { PersonIcon }
}
</script>

<style>
  #about {
    background-color: #fff;
    border-radius: 18px;
    box-shadow: rgba(100, 100, 111, 0.2) 0px 7px 29px 0px;
    padding: 1.8rem;
  }

  .about--top {
    display: flex;
    flex-direction: row;
    align-items: center;

    margin: 0 0 20px;
  }

  .about--icon-container {
    display: flex;
    justify-content: center;
    align-items: center;

    background-color: #f4f4f4;
    border-radius: 100%;
    height: 60px;
    width: 60px;
  }

  .about--icon {
    fill: #9096a0;
    height: 35px;
  }

  .about--text {
    margin: 0 0 0 10px;
  }

  .about--inputs-email {
    width: 100%;
  }

  .about--inputs-names {
    display: flex;
    flex-direction: row;
    justify-content: space-between;

    margin: 5px 0;
  }

  .about--inputs-first, .about--inputs-last {
    display: inline-block !important;
    width: 48%;
  }

  .about--button {
    background-color: #4a5dff;
    border: none;
    border-radius: 8px;
    color: #fff;
    cursor: pointer;
    font-size: 14px;
    font-weight: 600;
    display: block;
    padding: 10px 0;
    width: 100%;
  }
</style>
