<template>
  <div class="header text-white">
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
  height: var(--header-height) !important;
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
      const mapNavOptionsToPage = {
        Summary: {
          min: 2,
          max: 2,
        },
        Introduction: {
          min: 3,
          max: 5,
        },
        Bashroom: {
          min: 6,
          max: 10,
        },
        Mission: {
          min: 11,
          max: 17,
        },
        Achievements: {
          min: 18,
          max: 30,
        },
        Difficulties: {
          min: 31,
          max: 33,
        },
        Conclusion: {
          min: 34,
          max: 34,
        },
      };

      const pageRange = mapNavOptionsToPage[name];

      if (!pageRange) {
        return false;
      }

      return page >= pageRange.min && page <= pageRange.max;
    },
  },
  data() {
    return {
      navOptions: [
        "Summary",
        "Introduction",
        "Bashroom",
        "Mission",
        "Achievements",
        "Difficulties",
        "Conclusion",
      ],
    };
  },
};
</script>
