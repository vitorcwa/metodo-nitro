<template>
  <section id="faq" class="section section--gray">
    <div class="container">
      <span class="tag">Perguntas frequentes</span>
      <h2 class="title">Tire suas <em>dúvidas</em></h2>
      <div class="divider"></div>
      <div class="faq__list">
        <div v-for="(item, i) in faqs" :key="i" class="faq-item" :class="{ 'faq-item--open': openIndex === i }">
          <div class="faq-item__q" @click="toggle(i)">
            {{ item.q }}
            <span>+</span>
          </div>
          <div class="faq-item__a" v-show="openIndex === i">{{ item.a }}</div>
        </div>
      </div>
    </div>
  </section>
</template>

<script setup>
import { ref } from 'vue'

const openIndex = ref(null)
const toggle = (i) => { openIndex.value = openIndex.value === i ? null : i }

const faqs = [
  { q: 'Quanto tempo para ver os primeiros resultados?', a: 'Já no primeiro mês. A estratégia de arrancada (Quick Win) é ativada com prioridade — campanha no ar e processo rodando antes do mês acabar.' },
  { q: 'Preciso ter estrutura de marketing para contratar a CWA?', a: 'Não. A CWA foi desenhada para construir essa estrutura com você do zero. Diagnóstico completo, mapeamento da operação e implementação em fases organizadas.' },
  { q: 'O que é o Garage HUB?', a: 'O Garage HUB é a ferramenta de CRM automotivo desenvolvida pela CWA. Ele está incluído no plano e automatiza até 85% do processo comercial. É uma ferramenta dentro do Método N.I.T.R.O — não o método em si. O produto é o método aplicado pelo time CWA.' },
  { q: 'O plano inclui o investimento em mídia?', a: 'Não. O plano cobre todos os serviços da CWA — gestão, estratégia, tecnologia, treinamento e produção de conteúdo. O investimento em mídia (Meta/Google/TikTok) é definido separadamente.' },
  { q: 'O PDI é para todos os vendedores?', a: 'Sim, para todos os membros do time comercial — vendedores, pré-vendas e consignadores. Cada um recebe diagnóstico individual, trilha personalizada e acompanhamento de indicadores semana a semana.' },
  { q: 'Para qual tamanho de operação funciona?', a: 'Atendemos operações de diferentes tamanhos em todo o Brasil. O método se adapta ao seu estágio — o importante é que você já venda e queira crescer de forma estruturada e previsível.' },
]
</script>

<style scoped>
.faq__list { margin-top: 40px; max-width: 720px; }
.faq-item { border-bottom: 1px solid var(--bdr); padding: 18px 0; }
.faq-item__q { font-family: 'Space Grotesk', sans-serif; font-size: 15px; font-weight: 600; color: var(--ink); cursor: pointer; display: flex; justify-content: space-between; align-items: center; gap: 14px; }
.faq-item__q span { color: var(--g); font-size: 22px; flex-shrink: 0; line-height: 1; transition: transform .2s; font-weight: 300; }
.faq-item--open .faq-item__q span { transform: rotate(45deg); }
.faq-item__a { font-size: 14px; color: var(--sub); line-height: 1.75; margin-top: 10px; }
</style>
