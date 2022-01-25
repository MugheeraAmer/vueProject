<template>
  <div class="header-container">
    <section :class="{ colapseHeaderClass: colapseHeaderValue }">
      <div class="header-content" :class="{ hideHeaderClass: hideHeaderValue }">
        <h1>Heading</h1>
        <p>{{ heading_para }}</p>
      </div>
      <button @click="hideHeader">Hide header</button>
    </section>
  </div>
</template>

<script>
export default {
  name: "Header",
  props: [],
  data() {
    return {
      hideHeaderValue: false,
      colapseHeaderValue: false,
      heading_para: `Lorem ipsum dolor sit amet consectetur, adipisicing elit. Dicta, velit!
      Minima, sunt. Debitis enim illo maiores qui porro voluptatum eaque.`,
    };
  },
  methods: {
    hideHeader() {
      this.hideHeaderValue = !this.hideHeaderValue;
      this.colapseHeaderValue = !this.colapseHeaderValue;
    },
  },
};
</script>

<style scoped>
h1 {
  color: var(--secondary-color);
  margin: 3rem 0;
  font-size: 3rem;
}
p {
  margin: 3rem 0;
}

.header-content {
  display: flex;
  flex-direction: column;
  place-items: center;
  height: 80%;
  transition: all 2s ease;
}

button {
  width: 12rem;
  padding: 1rem 2rem;
  margin: 2rem 0;
  background: var(--secondary-color);
  color: white;
  font-size: 1rem;
  transition: all 500ms ease;
}

button:hover {
  background: var(--primary-color);
}
.hideHeaderClass {
  visibility: hidden;
  height: 0;
  margin: 0;
  opacity: 0;
  transition: all 2s ease;
}
section {
  display: flex;
  flex-direction: column;
  place-items: center;
  background: var(--ternary-color);
  height: 30rem;
  transition: all 3s ease;
}

.colapseHeaderClass {
  height: 6rem;
  transition: height 3s ease;
}
</style>
