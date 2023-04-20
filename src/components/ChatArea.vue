<template>
  <section class="inf_area">
    <h1>{{ h1 }}</h1>
  </section>
  <section class="chat_area">
    <div class="user" v-show="messages?.length != 0" v-for="(message, index) in messages" :key="index">
      <p class="identific">Você diz:</p>
      <p class="mensagem">{{ message }}</p>
    </div>
  </section>
</template>

<script>
export default {
  name: 'ChatArea',
  props: {
    h1: String,
    messages: {
      type: Array,
    }
  }
}

</script>

<style>
.inf_area {
  background: #4B4B4B;
  border-radius: 20px 20px 0px 0px;
  margin: 10px 0px -60px 0px;
}

h1 {
  font-family: 'Waiting for the Sunrise';
  font-style: normal;
  font-weight: 300;
  font-size: 36px;
  color: #B590E5;
  text-shadow: 0px 1px 5px #C090FC;
  padding: 20px 40px 40px 40px;
}

.chat_area {
  /* box */
  background: linear-gradient(180deg, #C5C5C5 5%, rgba(197, 197, 197, 0.109) 150%);
  box-shadow: 0px -5px 10px -4px #D9D9D9;
  border-radius: 20px;
  height: 550px;
  display: flex;
  flex-direction: column;
  padding: 40px;

  /*barra de rolagem*/
  overflow: auto;

  /* font */
  font-family: 'Lato';
  font-style: normal;
  font-weight: 400;
  font-size: 22px;
  line-height: 29px;
  color: #29292A;
}

.chat_area::-webkit-scrollbar {
  width: 5px;
}

.chat_area::-webkit-scrollbar-track {
  background-color: #292929;
  border-radius: 5px;
  margin: 15px;
}

.chat_area::-webkit-scrollbar-thumb {
  background-color: #B590E5;
  border-radius: 5px;
  margin: 15px;
}

.chat_area::-webkit-scrollbar-thumb:hover {
  background-color: #A16DE6;
  box-shadow: inset 0 0 6px #D9D9D9;
}

.atendente {
  display: flex;
  flex-direction: column;
  align-items: flex-start;
}

.user {
  display: flex;
  flex-direction: column;
  align-items: flex-end;
}

.mensagem {
  background: #B590E5;
  border-radius: 20px;
  width: 300px;
  height: 40px;
  margin: 10px 0px;
  padding: 10px 10px 0px 10px;
}

.identific {
  margin: 10px 0px;
  font-weight: bold;
}
</style>