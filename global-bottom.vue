<template>
  <div class="header p-1 text-white">
    <img class="logo" src="/logos/bashroom-logo-white.svg" />

    <ul class="header-nav">
      <li
        v-for="name of navOptions"
        :class="
          isCurrentPage(name, $slidev.nav.currentPage) ? 'active' : 'not-active'
        "
      >
        {{ name }}
      </li>
    </ul>
  </div>
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

.active {
  color: red;
  border-bottom: solid red;
}
</style>
<script>
export default {
  methods: {
    isCurrentPage(name, page) {
      const mapPageToNavOptions = [
        "",
        "Summary",
        "Introduction",
        "Introduction",
        "Bashroom",
        "Bashroom",
        "Bashroom",
        "Bashroom",
        "Bashroom",
        "Mission",
        "Mission",
        "Realisations",
        "Difficulties",
        "Conclusion",
      ];

      console.log(mapPageToNavOptions[page - 1], page);

      return mapPageToNavOptions[page - 1] === name;
    },
  },
  data() {
    return {
      navOptions: [
        "Summary",
        "Introduction",
        "Bashroom",
        "Mission",
        "Realisations",
        "Difficulties",
        "Conclusion",
      ],
    };
  },
};
</script>
