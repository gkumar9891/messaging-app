<template>
  <div class="messanger">
    <div>
     <div class="message">
      Lorem ipsum dolor sit, amet consectetur adipisicing elit. Commodi, ipsum?
     </div>
    </div>
    <div class="message">
      Lorem ipsum dolor sit amet consectetur adipisicing elit. Eius possimus
      iste deserunt eveniet aliquid voluptas temporibus aperiam doloremque vitae
      qui?
    </div>
    <div v-for="(message, index) in messages" :key="index">
        <span  class="message"> {{ message}} </span>
    </div>

    <form>
        <textarea v-model="message" ></textarea>
        <button type="button" @click="addMessage">Submit</button>
    </form>
  </div>
</template>

<script>
export default {
    name: 'MessamgerArea',
    data() {
        return  {
            message: '',
            messages: []
        }
    },
    methods: {
        addMessage() {
            this.messages.push(this.message);
            this.message = '';
        }
    }
};
</script>

<style scoped>
.messanger {
  width: 80%;
  height: calc(100vh - 100px);
  margin: auto;
  background: #000;
  overflow-y: auto;
  text-align: left;
  padding: 30px;

}

.message {
  padding: 5px;
  background-color: aqua;
  text-align: left;
  display: inline-block;
  margin-bottom: 10px;
}
</style>
