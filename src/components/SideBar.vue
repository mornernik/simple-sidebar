<template>
  <div>
    <button class="sidebar-toggle" @click="sideBarSet">Кнопка</button>
    <div class="bg-overlay is-hide" @click="sideBarSet"></div>
    <div class="sidebar is-closed">Текст</div>
  </div>
</template>

<script>
export default {
  data() {
    return {};
  },
  methods: {
    sideBarSet() {
      let toggleBtn = document.querySelector(".sidebar-toggle");
      let sidebar = document.querySelector(".sidebar");
      let bgOverlay = document.querySelector(".bg-overlay");
      toggleBtn.classList.toggle("is-closed");
      sidebar.classList.toggle("is-closed");
      bgOverlay.classList.toggle("is-hide");
    }
  }
};
</script>

<style scoped>
.sidebar-toggle {
  color: #000;
}

.bg-overlay {
  display: block;
  position: fixed;
  top: 0;
  right: 0;
  bottom: 0;
  left: 0;
  background-color: rgba(0, 0, 0, 0.2);
  z-index: 1;
}

.bg-overlay.is-hide {
  display: none;
}

.sidebar {
  width: 15em;
  height: 100vh;
  position: fixed;
  right: 0;
  top: 0;
  background-color: #e5e5e5;
  transition: 0.7s;
  z-index: 2;
}
.sidebar.is-closed {
  transform: translateX(16em);
}
</style>