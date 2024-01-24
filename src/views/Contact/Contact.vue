<template>
  <div>
    <div class="title">
      <h2>contato_</h2>
    </div>
    <div class="contact-content">
      <div>
        <p>Você pode entrar em contato comigo pelo email:</p>
        <h2>levi.andrew98@gmail.com</h2>
        <br />
        <p>Ou pode me encontrar em:</p>
        <div class="socialMedia">
          <a
            v-for="(item, index) in socialMedia"
            :key="index"
            :href="item.href"
            target="_blank"
          >
            <div
              :style="`background-image: url('${getImages(item.img)}')`"
            ></div>
          </a>
        </div>
      </div>
    </div>
  </div>
</template>

<script setup>
const socialMedia = [
  {
    name: 'Linkedin',
    img: 'linkedin.svg',
    href: 'https://www.linkedin.com/in/levi-andrew/',
  },
  {
    name: 'Github',
    img: 'github.svg',
    href: 'https://github.com/LeviAndrew',
  },
  {
    name: 'Whatsapp',
    img: 'whatsapp.svg',
    href: 'https://api.whatsapp.com/send?phone=5548999454663&text=Ol%C3%A1,%20Fiquei%20muito%20interessado%20em%20voc%C3%AA%20atrav%C3%A9s%20do%20seu%20portif%C3%B3lio!'
  }
]

function getImages(image) {
  return new URL(`../../assets/icons/${image}`, import.meta.url)
}
</script>

<style scoped lang="less" src="./Contacts.less"></style>
