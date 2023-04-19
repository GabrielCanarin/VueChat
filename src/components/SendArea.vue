<template>
  <ChatArea h1='Atendimento On-line' />
  <section class="send_area">
    <input type="text" id="txt_input" class="txt_input" placeholder="Digite sua mensagem..." v-model="message" />
    <button type="button" class="btn_send" @click="sendMessage">Enviar</button>
  </section>
</template>

<script>
import ChatArea from './ChatArea.vue'

export default {
  name: 'SendArea',
  components: {
    ChatArea
  },
  data() {
    return {
      messages: [],
    }
  },

  methods: {
    sendMessage() {
      if (this.message === '') {
        return
      }
      this.messages.push(this.message);
      this.message = '';
      console.log(this.messages);
    }

  }
}
</script>

<style>
.send_area {
  display: flex;
  justify-content: space-between;
  margin: 20px 0px;
}

.txt_input {
  /* box */
  width: 70%;
  height: 45px;
  background: #D9D9D9;
  box-shadow: 0px 4px 4px rgba(255, 255, 255, 0.25);
  border-radius: 20px;
  border: none;

  /* font */
  font-family: 'Waiting for the Sunrise';
  font-style: normal;
  font-weight: 300;
  font-size: 26px;
  line-height: 46px;
  padding: 0px 20px;
  color: #29292A;
}

.btn_send {
  /* box */
  width: 20%;
  height: 45px;
  background: #B590E5;
  box-shadow: 0px 4px 4px rgba(255, 255, 255, 0.25);
  border-radius: 20px;
  border: none;

  /* font */
  font-family: 'Waiting for the Sunrise';
  font-style: normal;
  font-weight: 300;
  font-size: 26px;
  line-height: 46px;
  padding: 0px 20px;
  color: #29292A;

  /* animation */
  transition: 100ms linear;
}

.btn_send:hover {
  transform: scale(1.05);
  background: #A16DE6;
}

.btn_send:active {
  background: #D9D9D9;
}
</style>