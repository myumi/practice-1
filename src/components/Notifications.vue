<template>
  <div id="notifications">
    <div class="notifications--icon-container">
      <BellIcon class="notifications--icon" alt="Bell with red dot on it" />
    </div>
    <div class="notifications--text">
      <h1>Turn on post notifications</h1>
      <h4>
        You can set up Chrome to get notifications, 
        like meeting reminders, from websites, apps, and
        extensions.
      </h4>
    </div>
    <button class="notifications--button" type="submit">Turn On</button>
  </div>
</template>

<script>
import BellIcon from './svgs/BellIcon.vue';

export default {
  name: 'Notifications',
  components: { BellIcon }
}
</script>

<style>
  #notifications {
    background-color: #fff;
    border-radius: 18px;
    box-shadow: rgba(100, 100, 111, 0.2) 0px 7px 29px 0px;
    padding: 1.8rem;
  }

  .notifications--icon-container {
    display: flex;
    align-items: center;
    justify-content: center;

    background-color: #f4f4f4;
    border-radius: 100%;
    height: 60px;
    width: 60px;
  }

  .notifications--icon {
    height: 30px;
  }

  .notifications--text {
    padding: 12px 0;
  }

  .notifications--text h1 {
    padding: 0 0 5px;
  }

  .notifications--button {
    background-color: #fff;
    border: 1px solid #4a5dff;
    border-radius: 8px;
    color: #4a5dff;
    cursor: pointer;
    font-size: 14px;
    font-weight: 600;
    display: block;
    padding: 10px 0;
    width: 100%;
  }
</style>
