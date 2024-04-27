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
        <button class="create-task-button" @click="tasks.push(1);" >Create <img src="src/assets/svg/plus.svg" alt=""></button>
      </div>

            <div class="tasks-wrapper">

              <div class="wrapper" >
                <div class="task-list-wrapper">
                  <p class="task-list-heading">Task list</p>
                  <span class="current-tasks-counter">0</span>
                </div>
                <div class="completed-task-wrapper">
                  <p class="completed-task-heading">Completed</p>
                  <span class="completed-tasks-counter">0</span>
                </div>
              </div>
              <span class="wrapper__underline"></span>

              <div class="empty-wrap" v-if="!tasks.length >= 1">
                <img class="clipboard-icon" src="../assets/svg/clipboard.svg" alt="">
                <p>
                  You don't have any tasks registered yet. <br><br>
                  Create tasks and organize your to-do items.
                </p>
              </div>

              <ToDoItem v-else />

            </div>

    </div>
</template>

<script setup>
  import {ref} from "vue";
  import ToDoItem from "@/widgets/ToDo/ui/ToDoItem.vue";
   const tasks = ref([])
</script>


<style lang="scss" scoped >

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
          height: 120px;
        }

        @include media($l){
          height: 200px;
        }

        .header__link {
          display: flex;
          gap: 12px;
        }

        .header__logo {
          height: 36px;
          padding-top: 10px;

          @include media($l){
            height: 56px;
            padding-top: 6px;
          }
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

          @include media($l){
            font-size: 64px;
          }

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
      top:25%;
      left:50%;
      transform:translate(-50%, -50%);


      @include media($xs){
        display: flex;
        justify-content: center;
        align-items: center;
        gap: 8px;
        position: absolute;
      }
      @include media($xs){
        top:22%;
      }

      @include media($l){
        top:26%;
      }

      .task-name-input {
        width: 640px;
        height: 54px;
        background-color: #262626;
        outline: none;
        border-radius: 8px;
        color: #ffffff;
        padding-left: 16px;
        border: 1px solid #0D0D0D;

        @include media($xs){
          width: 50dvw;
          height: 34px;
          font-size: 14px;
        }

        @include media($s){
          width: 60dvw;
          height: 42px;
          font-size: 14px;
        }

        @include media($m){
          width: 60dvw;
          height: 42px;
          font-size: 14px;
        }

        @include media($l){
          width: 640px;
          height: 54px;
          font-size: 14px;
        }
      }

      .task-name-input:focus::placeholder {
        color: transparent;
      }

      .task-name-input:hover {
        border: 1px solid ;
      }

      .create-task-button {

        border-radius: 8px;
        border: none;
        background-color: #1E6F9F;
        color: #ffffff;
        padding: 16px;
        display: flex;
        justify-content: center;
        align-items: center;
        gap: 8px;

        @include media($xs){
          padding: 10px;
          font-size: 14px;
        }

        @include media($s){
          padding: 14px;
          font-size: 14px;
        }

        @include media($l){
          padding: 16px;
          font-size: 18px;
          font-weight: 500;
          gap: 12px;
        }
      }
    }



    .tasks-wrapper {
      display: flex;
      flex-direction: column;
      justify-content: center;
      align-items: center;
      width: 100%;
      height: 290px;

      @include media($xs){
        margin-top: 160px;
      }


      .wrapper {
        display: flex;
        justify-content: center;
        width: 100%;


        @include media($xs){
          gap:60px;
        }
        @include media($s){
          gap:40dvw;
        }
        @include media($m){
          box-sizing: border-box;
          justify-content: space-between;
          max-width: 690px;
          gap: inherit;
        }
      }

      .wrapper__underline {

        width: 90%;
        max-width: 740px;
        border-bottom: 2px solid #333333;

      }

    }



    .task-list-wrapper {
      display: flex;
      align-items: center;
      gap: 8px;
    }

    .task-list-heading {
      color: #4EA8DE;
      width: 68px;
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
    }

    .clipboard-icon {
      width: 56px;
      height: 56px;
    }


</style>
