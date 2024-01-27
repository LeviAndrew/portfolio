<template>
  <footer>
    <div class="footer-content">
      <img src="../../../assets/images/logo-header.png" />
      <span>
        Esse portfólio foi desenvolvido por Levi Andrew, usando como referência o <a  href="https://github.com/guiialexandrino/"  target="_blank">github do gui</a>,
        utilizando:
      </span>
      <br />
      <div class="stack">
        <div
          v-for="(icon, index) in icons"
          :key="index"
          :style="`background-image: url(${getImage(icon)})`"
        ></div>
      </div>
      <span>Última atualização: 27/01/2024.</span>
    </div>
  </footer>
</template>

<script setup>
const icons = ['vuejs', 'language-javascript', 'html', 'css']
function getImage(file) {
  return new URL(`../../../assets/icons/${file}.svg`, import.meta.url)
}
</script>

<style lang="less" src="./Footer.less" />
