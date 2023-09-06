<template>
  <div class="hello">
    <h1>{{ msg }}</h1>
    <p>
      {{  my_message }}
    </p>

    <!-- <ul id=30 [...] > -->
    <ul v-bind:id="dynamicId" v-bind:class="myStyle">
      <li v-for="item in myArray" :key="item.id">
          <p> {{  item.message  }}</p>
      </li>
    </ul>

    <MyButton myText="Test 1"></MyButton>
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
      my_message: String,
      myArray: [ { id: 1, message: "Hello 1"} ],
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
