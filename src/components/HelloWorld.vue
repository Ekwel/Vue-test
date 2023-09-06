<template>
  <div class="hello">
    <h1>{{ msg }}</h1>
    <p>
      {{  my_message }}
    </p>

    <!-- <ul id=30 [...] > -->
    <div v-bind:id="dynamicId" v-bind:class="myStyle">
      <div v-for="item in myArray" :key="item.id">
          <p> {{  item.message  }}</p>
      </div>
    </div>

    <MyButton myText="Button 1"></MyButton>
  </div>
</template>

<script>

import MyButton from './base/MyButton.vue';

export default {
  name: 'HelloWorld',
  components: {
    MyButton
  },
  props: {
    msg: String,
    myStyle: String
  },
  data: function() {
    return {
      my_message: "Test",
      myArray: [ { id: 1, message: "[For] - Element 1"}, { id: 2, message: "[For] - Element 2"} ],
      dynamicId: 30
    }
  },

  methods: {
    init() {
      this.my_message = "Test"
    }
  }
}
</script>
