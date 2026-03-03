<template>
  <div id="cwa-app">
    <NavBar />
    <HeroSection />
    <LogosBand />
    <QuemSomos />
    <ProblemaSection />
    <MetodoNitro />
    <FunilSection />
    <PdiSection />
    <TreinamentosSection />
    <ResultadosSection />
    <GrandeQuote />
    <PlanoSection />
    <DepoimentosSection />
    <FaqSection />
    <CtaSection />
    <FooterSection />
  </div>
</template>

<script setup>
import NavBar from '@/components/NavBar.vue'
import HeroSection from '@/components/HeroSection.vue'
import LogosBand from '@/components/LogosBand.vue'
import QuemSomos from '@/components/QuemSomos.vue'
import ProblemaSection from '@/components/ProblemaSection.vue'
import MetodoNitro from '@/components/MetodoNitro.vue'
import FunilSection from '@/components/FunilSection.vue'
import PdiSection from '@/components/PdiSection.vue'
import TreinamentosSection from '@/components/TreinamentosSection.vue'
import ResultadosSection from '@/components/ResultadosSection.vue'
import GrandeQuote from '@/components/GrandeQuote.vue'
import PlanoSection from '@/components/PlanoSection.vue'
import DepoimentosSection from '@/components/DepoimentosSection.vue'
import FaqSection from '@/components/FaqSection.vue'
import CtaSection from '@/components/CtaSection.vue'
import FooterSection from '@/components/FooterSection.vue'
</script>

<style>
#cwa-app { min-height: 100vh; }
</style>
