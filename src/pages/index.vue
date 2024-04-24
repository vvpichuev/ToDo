<template>

    <div class="index-page">
        <header class="header">
          <a class="header__link" href="index.html">
            <img class="header__logo" src="src/assets/svg/rocket.svg" alt="logo"/>
            <h1 class="header__heading">to <span class="color-text">do</span></h1>
          </a>
        </header>

      <div class="new-task-field">
        <input class="task-name-input" type="text" placeholder="Type a new task">
        <button class="create-task-button" @click="tasks.push(1)" >Create <img src="src/assets/svg/plus.svg" alt=""></button>
      </div>
      <!--
            <div class="tasks-wrapper">

              <div class="wrapper">
                <div class="task-list-wrapper">
                  <p class="task-list-heading">Task list</p>
                  <span class="current-tasks-counter">0</span>
                </div>
                <div class="completed-task-wrapper">
                  <p class="completed-task-heading">Completed</p>
                  <span class="completed-tasks-counter">0</span>
                </div>
              </div>

              <div class="empty-wrap" v-if="!tasks.length">
                <img class="clipboard-icon" src="../assets/svg/clipboard.svg" alt="">
                <p>
                  You don't have any tasks registered yet. <br>
                  Create tasks and organize your to-do items.
                </p>
              </div>

              <div>

              </div>


            </div>

            -->
    </div>
</template>

<script setup>
  import {ref} from "vue";
   const tasks = ref([])
</script>


<style lang="scss" scoped >
//@import "@/assets/styles/scss/index";

    .index-page {
        width: 100%;
        height: 100dvh;
        background: #1A1A1A;
        color: #ffffff;
        font-family: Verdana, Geneva, Tahoma, sans-serif;
        display: flex;
        flex-direction: column;
        align-items: center;

      .header {
        display: flex;
        justify-content: center;
        align-items: center;
        width: 100%;
        height: 200px;
        background: #0D0D0D;
        position: relative;

        @include media($xs){
          height: 140px;
        }

        .header__link {
          display: flex;
          gap: 12px;
        }

        .header__logo {
          height: 36px;
          padding-top: 10px;
        }

        .header__heading {
          color: #4EA8DE;
          text-align: left;
          display: flex;
          justify-content: center;
          align-items: center;
          font-size: 40px;
          margin: 0;
          padding: 0;
          height: 48px;

          .color-text {
            color: #5E60CE;
          }
        }

      }
    }










    .new-task-field {
      display: flex;
      justify-content: center;
      align-items: center;
      gap: 8px;
      position: absolute;
      top: 170px;
      left: 470px;

      .task-name-input {
        width: 640px;
        height: 54px;
        background-color: #262626;
        outline: none;
        border-radius: 8px;
        color: #ffffff;
        padding-left: 16px;
        border: 1px solid #0D0D0D;
      }

      .task-name-input:focus::placeholder {
        color: transparent;
      }

      .task-name-input:hover {
        border: 1px solid ;
      }

      .create-task-button {
        width: 90px;
        height: 52px;
        border-radius: 8px;
        border: none;
        background-color: #1E6F9F;
        color: #ffffff;
        padding: 16px;
        display: flex;
        justify-content: center;
        align-items: center;
        gap: 8px;
      }
    }



    .tasks-wrapper {
      display: flex;
      flex-direction: column;
      justify-content: center;
      width: 740px;
      height: 290px;
      margin-top: 90px;

    }

    .wrapper {
      display: flex;
      justify-content: space-between;
    }

    .task-list-wrapper {
      display: flex;
      align-items: center;
      gap: 8px;
    }

    .task-list-heading {
    color: #4EA8DE;
    }

    .current-tasks-counter {
      background-color: #333333;
      padding: 2px 8px;
      border-radius: 99px;
    }

    .completed-task-wrapper {
      display: flex;
      align-items: center;
      gap: 8px;
    }

    .completed-task-heading {
      color: #8284FA;
    }

    .completed-tasks-counter {
      background-color: #333333;
      padding: 2px 8px;
      border-radius: 99px;
    }

    .empty-wrap {
      display: flex;
      flex-direction: column;
      justify-content: center;
      align-items: center;
      gap: 16px;
      padding: 64px 24px;
      text-align: center;
      border-top: 2px solid #333333;
    }

    .clipboard-icon {
      width: 56px;
      height: 56px;
    }


</style>
