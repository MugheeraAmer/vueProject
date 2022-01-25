<template>
  <nav>
    <ul>
      <li v-for="item in navbarList" :key="item">
        <a href="">{{ item }}</a>
      </li>
    </ul>
  </nav>
</template>

<script>
export default {
  name: "navbar",
  data() {
    return {
      navbarList: ["Home", "About Us", "Contact Us"],
    };
  },
};
</script>

<style scoped>
nav ul {
  display: flex;
  justify-content: center;
  width: 100vw;
  height: 3rem;
  list-style: none;
  background: var(--primary-color);
  font-size: 1rem;
}
nav ul li {
  padding: 1rem 1rem;
  background: var(--secondary-color);
}
nav ul li a {
  text-decoration: none;
  color: white;
}
</style>
