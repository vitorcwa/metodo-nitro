<template>
  <section class="section section--white">
    <div class="container">
      <span class="tag">Quem já acelerou com a CWA</span>
      <h2 class="title">Brindaremos juntos<br/><em>cada conquista</em></h2>
      <div class="divider"></div>
      <div class="testi__grid">
        <div v-for="t in testemunhos" :key="t.name" class="tstcard reveal">
          <div class="tstcard__stars">★ ★ ★ ★ ★</div>
          <p class="tstcard__text">"{{ t.text }}"</p>
          <div class="tstcard__author">
            <div class="tstcard__av">{{ t.initials }}</div>
            <div>
              <div class="tstcard__name">{{ t.name }}</div>
              <div class="tstcard__role">{{ t.role }}</div>
            </div>
          </div>
        </div>
      </div>
    </div>
  </section>
</template>

<script setup>
import { useScrollReveal } from '@/composables/useScrollReveal'
useScrollReveal('.reveal')

const testemunhos = [
  { initials: 'RA', name: 'Ricardo A.', role: 'Proprietário · Multimarca SP', text: 'Antes da CWA, a gente perdia lead toda hora. Hoje o processo responde, agenda e faz follow-up sozinho. Nossa taxa de conversão dobrou em 3 meses.' },
  { initials: 'MF', name: 'Marcelo F.', role: 'Gerente Comercial · Concessionária RJ', text: 'O que me convenceu foi a estrutura. Não é só agência de marketing — é metodologia, treinamento de equipe e sistema. Ninguém mais entrega isso no automotivo.' },
  { initials: 'PS', name: 'Paulo S.', role: 'Proprietário · Multimarca MG', text: 'A reativação de base da CWA foi uma surpresa. Fechamos 8 vendas em duas semanas — sem gastar mais um centavo em tráfego. Base é ativo, não estava usando.' },
]
</script>

<style scoped>
.testi__grid { display: grid; grid-template-columns: repeat(3,1fr); gap: 14px; margin-top: 48px; }
.tstcard { background: #fff; border: 1px solid var(--bdr); border-radius: 12px; padding: 24px; transition: all .25s; opacity: 0; transform: translateY(14px); }
.tstcard.revealed { opacity: 1; transform: translateY(0); transition: opacity .5s ease, transform .5s ease; }
.tstcard:hover { box-shadow: var(--sh2); transform: translateY(-3px); }
.tstcard__stars { color: #F5A623; font-size: 12px; letter-spacing: 3px; margin-bottom: 11px; }
.tstcard__text { font-size: 14px; color: var(--sub); line-height: 1.7; font-style: italic; margin-bottom: 16px; }
.tstcard__author { display: flex; align-items: center; gap: 9px; }
.tstcard__av { width: 34px; height: 34px; border-radius: 50%; background: linear-gradient(135deg, #18B25A, #34D680); display: flex; align-items: center; justify-content: center; font-weight: 700; font-size: 12px; color: #fff; }
.tstcard__name { font-family: 'Space Grotesk', sans-serif; font-size: 13px; font-weight: 600; color: var(--ink); }
.tstcard__role { font-size: 11px; color: var(--muted); }
@media (max-width: 900px) { .testi__grid { grid-template-columns: 1fr; } }
</style>
