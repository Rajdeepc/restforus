<template>
  <div class="mx-auto">
    <div class="flex flex-row mb-24 items-center">

      <div class="flex-auto items-center">
        <div class="text-center text-5xl font-extrabold leading-none tracking-tight">
          <span
            class="bg-clip-text text-transparent bg-gradient-to-r from-teal-400 to-blue-500"
          >teleport</span>
        </div>
        <h5>A super simplified Rest client for H U M A N S</h5>
      </div>
       <div class="flex-auto items-end">
         <img :src="herobanner" />
      </div>



    </div>


    <div class="flex flex-row mb-32 justify-center">
      <div class="items-center">
        <button
          class="p-5 getstartedbtn rounded-md py-3 px-8"
          v-on:click="goto('https://teleportz.herokuapp.com/')"
        >Get Started</button>
      </div>
      <div class="items-center">
        <button
          class="p-5 githubbtn rounded-md py-3 px-8"
          v-on:click="goto('https://github.com/Rajdeepc/teleport')"
        >Github</button>
      </div>
    </div>
    <div class="rounded-t-lg overflow-hidden shadow-2xl">
      <img :src="bannerImg" />
    </div>
    <div class="subscribe">
      <h3>Keep yourself updated with new feature releases.</h3>
      <div class="flex flex-row">
        <div>
          <input type="email" placeholder="Your Email Address.." />
        </div>
        <div>
          <button class="p-5 getstartedbtn rounded-md py-3 px-8">Subscribe</button>
        </div>
      </div>
    </div>
  </div>
</template>

<script>
import { herobanner, bannerImg } from "../assets/images/images";

export default {
  name: "HelloWorld",
  data() {
    return {
      bannerImg,
      herobanner
    };
  },
  props: {
    msg: String,
  },
  methods: {
    goto: function (params) {
      window.open(params, "_blank");
    },
  },
};
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>
h3 {
  margin: 40px 0 0;
}
ul {
  list-style-type: none;
  padding: 0;
}
li {
  display: inline-block;
  margin: 0 10px;
}
a {
  color: #42b983;
}
.getstartedbtn {
  background: #673ab7;
  color: white;
}
.githubbtn {
  background: gray;
  color: white;
}
.backbanner{
  background: url('../assets/images/herobanner.png');
      height: 600px;
    background-size: cover;
    background-repeat: no-repeat;

}
</style>
