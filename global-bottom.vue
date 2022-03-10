<template>
  <div class="header p-1 text-white">
    <img class="logo" src="/logos/bashroom-logo-white.svg" />

    <!-- Bashroom Icon -->

    <ul class="header-nav">
      <li @mouseover="mouseenterFunc">Home</li>
      <li @mouseover="mouseenterFunc">Summary</li>
      <li @mouseover="mouseenterFunc">Bashroom</li>
      <li @mouseover="mouseenterFunc">Mission</li>
      <li @mouseover="mouseenterFunc">Realisations</li>
      <li @mouseover="mouseenterFunc">Difficulties</li>
      <li @mouseover="mouseenterFunc">Conclusion</li>
    </ul>
  </div>
  <span class="target"></span>
</template>
<style>
.header {
  background: black;
  display: flex;
}

.logo {
  width: 32px;
  height: 32px;
  margin: 16px;
}

.header-nav {
  display: flex;
  justify-content: center;
  flex-wrap: wrap;
  margin-top: 12px;
}
.header-nav li {
  display: block;
  font-size: 20px;
  text-decoration: none;
  padding: 7px 15px;
}

.target {
  position: absolute;
  border-bottom: 4px solid transparent;
  top: 5px;
}

.header-nav li,
.target {
  transition: all 0.35s ease-in-out;
}
</style>
<script>
export default {
  methods: {
    mouseenterFunc(event) {
      const eventTarget = event.target;

      const width = eventTarget.getBoundingClientRect().width;
      const height = eventTarget.getBoundingClientRect().height;
      const left = eventTarget.getBoundingClientRect().left;

      const target = document.querySelector(".target");

      target.style.width = `${width}px`;
      target.style.height = `${height}px`;
      target.style.left = `${left}px`;
      target.style.borderColor = "red";
    },
  },
};

// function mouseenterFunc() {
//   if (!this.parentNode.classList.contains("active")) {
//     // code here
//   }
// }
</script>
