<template>
  <footer class="footer absolute bottom-0 left-0 right-0">
    <span class="footer-tutor text-white">Intership Tutor: Hadrien Toma</span>
    <span class="footer-copyright text-white">Copyright © Bashroom</span>
    <div class="footer-author">
      <span class="footer-author-name text-white"
        >Guillaume Mailhol - Epitech 2024</span
      >
      <img class="footer-author-icon" src="/logos/epitech-logo.png" />
    </div>
  </footer>
</template>

<style>
.footer {
  height: var(--footer-height);
  display: flex;
  padding-left: 20px;
  padding-right: 20px;
  justify-content: space-between;
  border-top: solid 2px grey;
  background-color: black;
}

.footer-tutor {
  display: flex;
  align-items: center;
  font-size: 12px;
}

.footer-copyright {
  display: flex;
  align-items: center;
}

.footer-author {
  display: flex;
  align-items: center;
}

.footer-author-name {
  font-size: 12px;
  margin-right: 6px;
}

.footer-author-icon {
  width: 128px;
}
</style>
