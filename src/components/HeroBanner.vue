<template>
  <div>
    <div class="flex justify-around items-center">
      <div>
        <div class="mb-3 text-left font-extrabold leading-none tracking-tight">
          <span
            class="text-lg bg-clip-text text-transparent bg-gradient-to-r from-teal-400 to-blue-500"
          >Pegasus</span>
        </div>
        <h5 class="mb-8 text-left">A simplified Rest client designed for H U M A N S</h5>
        <div class="flex flex-row justify-between">
          <div class="items-start w-full mr-5">
            <button
              class="p-5 getstartedbtn rounded-md py-3 px-8 w-full"
              v-on:click="goto('https://Pegasusz.herokuapp.com/')"
            >Get Started</button>
          </div>
          <div class="items-start w-full">
            <button
              class="p-5 githubbtn rounded-md py-3 px-8 w-full"
              v-on:click="goto('https://github.com/Rajdeepc/Pegasus')"
            >Github</button>
          </div>
        </div>
      </div>
      <div>
        <img :src="herobanner" />
      </div>
    </div>

    <div class="container py-32 mx-auto">
      <div>
        <div class="rounded-t-lg overflow-hidden shadow-2xl mb-32">
          <img :src="bannerImg" />
        </div>
      </div>
      <div class="features mb-24">
        <p class="mb-16 text-5xl">Features</p>
        <div class="grid grid-cols-3 gap-4">
          <div class="flex flex-col mb-16 items-center">
            <div class="mb-6">
              <img :src="content1" />
            </div>
            <div>
              <p>Compare Response Feature will help in comparing two different response of same API</p>
            </div>
          </div>
          <div class="flex flex-col mb-16 items-center">
            <div class="mb-6">
              <img :src="content2" />
            </div>
            <div>
              <p>Notification Switch will enable the user to get notifications on any change in API response in real time</p>
            </div>
          </div>
          <div class="flex flex-col mb-16 items-center">
            <div class="mb-6">
              <img :src="content3" />
            </div>
            <div>
              <p>Code Generator helps in generating API methods so that you can use it in your project. It supports curl, NodeJS, Perl</p>
            </div>
          </div>
          <div class="flex flex-col mb-16 items-center">
            <div class="mb-6">
              <img :src="content4" />
            </div>
            <div>
              <p>Personalized Settings is enabled to give user more power to customize the application according to his needs</p>
            </div>
          </div>
          <div class="flex flex-col mb-16 items-center">
            <div class="mb-6">
              <img :src="content5" />
            </div>
            <div>
              <p>Difference checker switch helps to show only attribute difference or value difference</p>
            </div>
          </div>
          <div class="flex flex-col mb-16 items-center">
            <div class="mb-6">
              <img :src="content6" />
            </div>
            <div>
              <p>IndexDB Support holds your settings local to your system so that it is not lost</p>
            </div>
          </div>
        </div>
      </div>
      <div class="subscribe">
          <p class="text-5xl">Subscribe</p>
          <p class="mb-8">Keep yourself updated with new feature releases.</p>
          <div class="flex flex-row justify-center items-center mb-4">
            <div>
              <input
                type="email"
                class="border-gray-400 border-solid p-3 border"
                placeholder="Your Email Address.."
              />
              
            </div>
            <div>
              <button class="p-5 getstartedbtn rounded-md py-3 px-8" v-on:click="onClickSubscribed">Subscribe</button>
            </div>
          </div>
          <p v-if="isSubscribed" class="indigo">Thank you for subscribing.</p>
        </div>
      
  
    </div>
    <footer>
          <div>
        <p class="mb-4">Made with <i class="fa fa-heart" aria-hidden="true"></i> by Rajdeep Chandra</p>
        <div class="flex flex-row items-center justify-center">
          <div class="mr-2">
            <a href="https://github.com/Rajdeepc" target="_blank">
              <i class="fa fa-github fa-2x" aria-hidden="true"></i>
            </a>
          </div>
          <div class="mr-2">
            <a href="https:twitter.com/@rajrock38" target="_blank">
              <i class="fa fa-twitter fa-2x" aria-hidden="true"></i>
            </a>
          </div>
          <div class="mr-2">
            <a href="https:medium.com/@rajrock38" target="_blank">
              <i class="fa fa-medium fa-2x" aria-hidden="true"></i>
            </a>
          </div>
        </div>
      </div>
    </footer>
  </div>
</template>

<script>
import {
  herobanner,
  bannerImg,
  content1,
  content2,
  content3,
  content4,
  content5,
  content6,
} from "../assets/images/images";

export default {
  name: "HelloWorld",
  data() {
    return {
      bannerImg,
      herobanner,
      content1,
      content2,
      content3,
      content4,
      content5,
      content6,
      isSubscribed:false
    };
  },
  props: {
    msg: String,
  },
  methods: {
    goto: function (params) {
      window.open(params, "_blank");
    },
    onClickSubscribed: function() {
      this.isSubscribed = true
    }
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
.backbanner {
  background: url("../assets/images/herobanner.png");
  height: 600px;
  background-size: cover;
  background-repeat: no-repeat;
}
.text-lg{
  font-size: 6rem;
}
</style>
