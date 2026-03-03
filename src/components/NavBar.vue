<template>
  <nav :class="['navbar', { 'navbar--scrolled': scrolled }]">
    <div class="container navbar__inner">
      <a href="#" class="navbar__logo">
        <img src="../../public/assets/img/logo.webp" alt="CWA Digital" />
      </a>
      <ul class="navbar__links">
        <li><a href="#quem">Quem somos</a></li>
        <li><a href="#metodo">N.I.T.R.O</a></li>
        <li><a href="#pdi">PDI</a></li>
        <li><a href="#plano">Plano</a></li>
        <li><a href="#faq">FAQ</a></li>
      </ul>
      <a href="#diagnostico" class="btn btn--green navbar__cta">🚀 Diagnóstico gratuito</a>
      <button class="navbar__burger" @click="menuOpen = !menuOpen" aria-label="Menu">
        <span></span><span></span><span></span>
      </button>
    </div>
    <div v-if="menuOpen" class="navbar__mobile">
      <a href="#quem" @click="menuOpen=false">Quem somos</a>
      <a href="#metodo" @click="menuOpen=false">N.I.T.R.O</a>
      <a href="#pdi" @click="menuOpen=false">PDI</a>
      <a href="#plano" @click="menuOpen=false">Plano</a>
      <a href="#faq" @click="menuOpen=false">FAQ</a>
      <a href="#diagnostico" class="btn btn--green" @click="menuOpen=false">🚀 Diagnóstico gratuito</a>
    </div>
  </nav>
</template>

<script setup>
import { ref, onMounted, onUnmounted } from 'vue'
const scrolled = ref(false)
const menuOpen = ref(false)
const onScroll = () => { scrolled.value = window.scrollY > 20 }
onMounted(() => window.addEventListener('scroll', onScroll))
onUnmounted(() => window.removeEventListener('scroll', onScroll))
</script>

<style scoped>
.navbar {
  position: fixed; top: 0; left: 0; right: 0; z-index: 100;
  border-bottom: 1px solid var(--bdr);
  background: rgba(244,249,246,.94);
  backdrop-filter: blur(20px);
  transition: box-shadow .2s;
}
.navbar--scrolled { box-shadow: 0 2px 24px rgba(0,0,0,.07); }
.navbar__inner {
  display: flex; align-items: center; justify-content: space-between; height: 66px;
}
.navbar__logo img { height: 30px; object-fit: contain; display: block; }
.navbar__links {
  display: flex; gap: 30px; list-style: none;
}
.navbar__links a {
  color: var(--sub); text-decoration: none; font-size: 13px; font-weight: 500; transition: color .2s;
}
.navbar__links a:hover { color: var(--g); }
.navbar__cta { font-size: 13px; padding: 10px 20px; }
.navbar__burger {
  display: none; flex-direction: column; gap: 5px;
  background: none; border: none; cursor: pointer; padding: 4px;
}
.navbar__burger span { display: block; width: 22px; height: 2px; background: var(--ink); border-radius: 2px; }
.navbar__mobile {
  display: flex; flex-direction: column; gap: 4px;
  padding: 16px 20px; border-top: 1px solid var(--bdr); background: var(--white);
}
.navbar__mobile a {
  color: var(--sub); text-decoration: none; font-size: 15px; font-weight: 500;
  padding: 10px 0; border-bottom: 1px solid var(--bdr);
}
.navbar__mobile .btn { margin-top: 10px; text-align: center; justify-content: center; }
@media (max-width: 900px) {
  .navbar__links, .navbar__cta { display: none; }
  .navbar__burger { display: flex; }
}
</style>
