<template>
  <div class="landing">
    <transition name="fade">
      <span class="name-loc" v-show="display1">
        Jason-S-Wang
        <a id="stf" href="https://eecs.berkeley.edu">@Stanford</a>
        <a id="ucb" href="https://eecs.berkeley.edu"><s>@UC-Berkeley</s></a>
      </span>
    </transition>
    <transition name="fade">
      <span v-show="display2">:</span>
    </transition>
    <transition name="fade">
      <span class="curly" v-show="display2">~ </span>
    </transition>
    <transition name="fade">
      <span class="dollar-sign" v-show="display3">$ </span>
    </transition>
    <span class="code">{{ welcomeText.slice(0, idx) }}</span>
    <span class="cursor" v-show="display4">&nbsp;&nbsp;</span>
  </div>
</template>

<script>
export default {
  name: "Landing",
  data() {
    return {
      display1: false,
      display2: false,
      display3: false,
      display4: false,
      welcomeText: "Welcome. ",
      idx: 0,
    };
  },
  mounted() {
    var v = this;
    setTimeout(function () {
      v.display1 = true;
    }, 500);
    setTimeout(function () {
      v.display2 = true;
    }, 1000);
    setTimeout(function () {
      v.display3 = true;
    }, 1500);
    setTimeout(function () {
      v.display4 = true;
    }, 2000);
    setTimeout(function () {
      var interval = setInterval(function () {
        if (v.idx >= v.welcomeText.length) {
          clearInterval(interval);
          return;
        }
        v.idx += 1;
      }, 200);
    }, 2300);
  },
};
</script>

<style scoped>
.landing {
  background: linear-gradient(rgba(0, 0, 0, 0.3), rgba(0, 0, 0, 0.3)),
    url(../assets/landing.jpg);
  background-size: cover;
  background-repeat: no-repeat;
  background-position: center center;
  padding: 8rem 3rem;
  text-align: left;
}

.landing > span {
  font-size: 5rem;
  color: white;
  margin: 0;
  font-size: 2.5rem;
  font-weight: 500;
}

.name-loc {
  color: #47dadf !important;
}

#ucb {
  text-decoration: none;
  color: #fdb515;
}

#ucb:hover {
  color: #f5c152;
}

#stf {
  text-decoration: none;
  text-shadow: 0 0 5px #000000;
  color: #8c1515;
}

#stf:hover {
  text-decoration: none;
  color: #b83a4b;
}

/* .curly {
  color: #fdb515 !important;
} */

.dollar-sign,
.code {
  font-weight: 600 !important;
}

.cursor {
  background-color: white;
  animation: blink 1s infinite;
}

.fade-enter-active,
.fade-leave-active {
  transition: opacity 1s ease-in-out;
}

.fade-enter-from,
.fade-leave-to {
  opacity: 0;
}

@keyframes blink {
  0% {
    background-color: white;
  }
  49% {
    background-color: white;
  }
  50% {
    background-color: transparent;
  }
  99% {
    background-color: transparent;
  }
}
</style>