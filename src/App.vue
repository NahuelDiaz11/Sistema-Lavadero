<template>
  <div>
    <Navbar />

    <img
      alt="Vue logo"
      class="logo"
      src="@/assets/logo.svg"
      width="125"
      height="125"
    />

    <form
      action="mailto:tuemail@ejemplo.com"
      method="post"
      enctype="text/plain"
    >
      Nombre:<br />
      <input type="text" name="nombre" /><br />
      Teléfono:<br />
      <input type="text" name="telefono" /><br />
      Email:<br />
      <input type="text" name="email" /><br />
      Comentario:<br />
      <textarea name="comentario"></textarea><br /><br />
      <input type="submit" value="Enviar" />
    </form>
  </div>
</template>

<script>
import { defineAsyncComponent } from "vue";
import { RouterLink, RouterView } from "vue-router";
import Navbar from "./components/Navbar.vue";

export default {
  components: {
    Navbar: defineAsyncComponent(() => import("./components/Navbar.vue")),
  },
};
</script>

<style scoped>
header {
  line-height: 1.5;
  max-height: 100vh;
}

.logo {
  display: block;
  margin: 0 auto 2rem;
}

nav {
  width: 100%;
  font-size: 12px;
  text-align: center;
  margin-top: 2rem;
}

nav a.router-link-exact-active {
  color: var(--color-text);
}

nav a.router-link-exact-active:hover {
  background-color: transparent;
}

nav a {
  display: inline-block;
  padding: 0 1rem;
  border-left: 1px solid var(--color-border);
}

nav a:first-of-type {
  border: 0;
}

@media (min-width: 1024px) {
  header {
    display: flex;
    place-items: center;
    padding-right: calc(var(--section-gap) / 2);
  }

  .logo {
    margin: 0 2rem 0 0;
  }

  header .wrapper {
    display: flex;
    place-items: flex-start;
    flex-wrap: wrap;
  }

  nav {
    text-align: left;
    margin-left: -1rem;
    font-size: 1rem;

    padding: 1rem 0;
    margin-top: 1rem;
  }
}
</style>
