<template>
  <div id="app">
    <nav>
      <router-link to="/">
        <div class="navigation__logo">Twotter</div>
      </router-link>
      <div class="navigation__user">
        {{ state.user.username }}
      </div>
    </nav>
    <router-view />
  </div>
</template>

<script>
import { reactive } from "vue";
export default {
  name: "App",
  setup() {
    const state = reactive({
      user: {
        username: "Garan",
      },
    });
    // const user = computed(() => store.state.User.user);
    return {
      state,
    };
  },
};
</script>

<style lang='scss'>
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  line-height: 1.5em;
  color: #2c3e50;
  min-height: 100vh;
  background-color: #f3f5fa;

  nav {
    display: flex;
    align-items: center;
    justify-content: space-between;
    padding: 10px 5%;
    background-color: rebeccapurple;
    color: white;

    .navigation__logo {
      font-weight: bold;
      font-size: 24px;
    }

    .navigation__user {
      font-weight: bold;
    }
  }
}
</style>
