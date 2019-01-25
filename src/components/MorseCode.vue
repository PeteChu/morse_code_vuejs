<template>
  <div>
    <h1>Hello Morse Code</h1>
    <h3>Message</h3>
    <input type="text" v-model="message" v-on:input="toMorse(message)">
    <h3>Encoded Message</h3>
    <h4>{{morseEncoded}}</h4>
  </div>
</template>

<script>
import morseJson from "./../../static/morseCode.json";
export default {
  name: "MorseCode",
  data: function() {
    return {
      morseCode: morseJson,
      message: "",
      morseEncoded: ""
    };
  },
  methods: {
    toMorse: function(s) {
      this.morseEncoded = "";
      for (var i of s.toLowerCase()) {
        if (i == " ") {
          this.morseEncoded += "/ ";
        } else {
          this.morseEncoded += this.morseCode[i] + " ";
        }
      }
    }
  }
};
</script>

