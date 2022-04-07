<template>
  <div>
    <h1>Drumkit</h1>
    <div class="keys">
      <Key v-for="(key, i) in keys" :sound="key" :key="i" />
    </div>

    <div class="piano">
      <h1>Piano</h1>
       <div class="keys">
      <Key v-for="(piano, i) in pianos" :sound="piano" :key="i" />
    </div>
    </div>
  </div>
</template>

<script>
import Key from "./components/Key.vue";
export default {
  name: "App",

  data() {
    return {
      keys: [
        {
          name: "boom",
          audio: require("./assets/sounds/boom.wav"),
          letter: "A",
        },
        {
          name: "clap",
          audio: require("./assets/sounds/clap.wav"),
          letter: "S",
        },
        {
          name: "hihat",
          audio: require("./assets/sounds/hihat.wav"),
          letter: "D",
        },
        {
          name: "kick",
          audio: require("./assets/sounds/kick.wav"),
          letter: "F",
        },
        {
          name: "openhat",
          audio: require("./assets/sounds/openhat.wav"),
          letter: "G",
        },
        {
          name: "ride",
          audio: require("./assets/sounds/ride.wav"),
          letter: "H",
        },
        {
          name: "snare",
          audio: require("./assets/sounds/snare.wav"),
          letter: "J",
        },
        {
          name: "tink",
          audio: require("./assets/sounds/tink.wav"),
          letter: "K",
        },
        {
          name: "tom",
          audio: require("./assets/sounds/tom.wav"),
          letter: "L",
        },
      ],
      pianos: [
        {
          name: "key1",
          audio: require("./assets/paino/key01.ogg"),
          letter: "Z",
        },
        {
          name: "key2",
          audio: require("./assets/paino/key02.ogg"),
          letter: "X",
        },
        {
          name: "key3",
          audio: require("./assets/paino/key03.ogg"),
          letter: "C",
        },
        {
          name: "key4",
          audio: require("./assets/paino/key04.ogg"),
          letter: "V",
        },
        {
          name: "key5",
          audio: require("./assets/paino/key05.ogg"),
          letter: "B",
        },
        {
          name: "key6",
          audio: require("./assets/paino/key06.ogg"),
          letter: "N",
        },
        {
          name: "key7",
          audio: require("./assets/paino/key07.ogg"),
          letter: "M",
        },
      ],
    };
  },
  components: { Key },
  setup() {
    return {
      Key,
    };
  },
};
</script>

<style>
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  margin-top: 60px;
}

.keys {
  display: flex;
  align-items: center;
  justify-content: center;
  border-bottom: #ccc solid 1px;
  padding: 60px;
}

.piano {
  padding-top: 70px;
}
</style>
