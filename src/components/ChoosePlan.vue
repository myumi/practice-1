<template>
  <div id="choose-plan">
    <h1>Choose a plan</h1>
    <h4>
      We make it simple. 
      Pay as you go or make the yearly commitment
      and gain the most flexibility.
    </h4>

    <Plans />

    <h2 class="choose-plan--payment-header">Payment details</h2>
    <div class="choose-plan--payment-selection">
      <div class="payment--cc">
        <div class="payment--left">
          <div class="payment--cc-image"></div>
          <div class="payment--text">
            <h5>Credit Card</h5>
            <span>7664 **** **** 9876</span>
          </div>
        </div>
        <button class="payment--button">cvc</button>
      </div>

      <div class="payment--paypal">
        <div class="payment--left">
          <div class="payment--paypal-image"></div>
          <div class="payment--text">
            <h5>Paypal</h5>
            <span>john@gmail.com</span>
          </div>
        </div>
        <button class="payment--button">cvc</button>
      </div>
    </div>
    <span class="choose-plan--add-payment">Add payment method</span>

    <input class="choose-plan--email-input" type="text" placeholder="Email Address" />

    <button class="choose-plan--email-button" type="submit">Email Address</button>
  </div>
</template>

<script>
import Plans from './Plans.vue'

export default {
  name: 'ChoosePlan',
  components: { Plans }
}
</script>

<style>
  #choose-plan {
    background-color: #fff;
    border-radius: 18px;
    box-shadow: rgba(100, 100, 111, 0.2) 0px 7px 29px 0px;
    padding: 1.8rem;
  }

  #choose-plan h1 {
    margin: 0 0 8px;
  }

  .choose-plan--payment-selection {
    display: flex;
    flex-direction: column;

    margin: 8px 0;
  }

  .payment--cc, .payment--paypal {
    display: flex;
    flex-direction: row;
    align-items: center;
    justify-content: space-between;

    margin: 8px 0 0;
  }

  .payment--left {
    display: flex;
    flex-direction: row;
  }

  .payment--text {
    margin: 0 0 0 10px;
  }

  .payment--text h5 {
    font-size: 12px;
  }

  .payment--text span {
    color: #999fa7;
    font-size: 10px;
  }

  .payment--cc-image, .payment--paypal-image {
    background-color: #f4f4f4;
    border-radius: 5px;
    height: 35px;
    width: 50px;
  }

  .payment--button {
    background-color: #fff;
    border: 1px solid #e7e7e7;
    border-radius: 6px;
    color: #8d939e;
    cursor: pointer;
    height: 30px;
    width: 50px;
  }

  .choose-plan--add-payment {
    color: #4a5dff;
    cursor: pointer;
    display: block;
    font-size: 10px;
    font-weight: 800;
    text-transform: uppercase;
  }

  .choose-plan--email-input {
    width: 100%;
    margin: 30px 0 20px !important;
  }

  .choose-plan--email-button {
    background-color: #4a5dff;
    border: none;
    border-radius: 8px;
    color: #fff;
    cursor: pointer;
    font-size: 14px;
    font-weight: 600;
    display: block;
    padding: 22px 0;
    width: 100%;
  }
</style>