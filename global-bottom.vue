<template>
  <div class="header p-1">
    <img class="header-icon" />
    <!-- Bashroom Icon -->

    <ul class="header-nav">
      <li @mouseover="mouseenterFunc">Home</li>
      <li @mouseover="mouseenterFunc">Summary</li>
      <li @mouseover="mouseenterFunc">Bashroom</li>
      <li @mouseover="mouseenterFunc">Mission</li>
      <li @mouseover="mouseenterFunc">Realisations</li>
      <li @mouseover="mouseenterFunc">Difficulties</li>
      <li @mouseover="mouseenterFunc">Conclusion</li>
      <span class="target"></span>
    </ul>
  </div>
</template>
<style>
.header {
  background: black;
}

.header-nav {
  display: flex;
  justify-content: center;
  flex-wrap: wrap;
}
.header-nav li {
  display: block;
  font-size: 20px;
  color: black;
  text-decoration: none;
  padding: 7px 15px;
}

.target {
  position: absolute;
  border-bottom: 4px solid transparent;
  z-index: -1;
  transform: translateX(-60px);
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
      const top = eventTarget.getBoundingClientRect().top;
      const color = colors[Math.floor(Math.random() * colors.length)];

      target.style.width = `${width}px`;
      target.style.height = `${height}px`;
      target.style.left = `${left}px`;
      target.style.top = `${top}px`;
      target.style.borderColor = color;
      target.style.transform = "none";
    },
  },
};

// function mouseenterFunc() {
//   if (!this.parentNode.classList.contains("active")) {
//     // code here
//   }
// }
</script>
