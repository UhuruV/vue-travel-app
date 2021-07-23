<template>
  <div>
    <nav id="nav">
      <ul class="nav-links">
        <li class="destination">
          <router-link to="/" class="links"> Home</router-link>
        </li>
        <li
          v-for="destination in destinations"
          :key="destination.name"
          class="links"
        >
          <router-link
            :to="{
              name: 'DestinationDetails',
              params: { slug: destination.slug }
            }"
          >
            {{ destination.name }}
          </router-link>
        </li>
      </ul>
    </nav>
  </div>
</template>

<script>
import store from "@/store";
export default {
  data() {
    return {
      destinations: store.destinations
    };
  }
};
</script>

<style scoped>
#nav {
  display: flex;
}
#nav a {
  font-weight: bold;
  text-decoration: none;
  color: #000;
}

#nav a.router-link-exact-active {
  color: #eb34e8;
}
.nav-links {
  display: flex;
}
.links {
  padding-right: 20px;
  /* text-decoration: none; */
  list-style: none;
}
.links:hover {
  text-decoration: underline;
}
</style>
