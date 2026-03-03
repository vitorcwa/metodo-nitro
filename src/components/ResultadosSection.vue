<template>
  <section class="section section--white">
    <div class="container">
      <span class="tag">O que entregamos</span>
      <h2 class="title">Resultados reais<br/><em>para a sua multimarcas</em></h2>
      <p class="subtitle">Marketing, automação e treinamento são as ferramentas. O que entregamos é uma operação eficiente, lucrativa e sustentável — que te dá tempo, previsibilidade e liberdade.</p>
      <div class="divider"></div>
      <div class="res__grid">
        <div v-for="r in resultados" :key="r.title" class="rcard reveal">
          <div class="rcard__ic">{{ r.icon }}</div>
          <h3>{{ r.title }}</h3>
          <p>{{ r.desc }}</p>
        </div>
      </div>
    </div>
  </section>
</template>

<script setup>
import { useScrollReveal } from '@/composables/useScrollReveal'
useScrollReveal('.reveal')

const resultados = [
  { icon: '💰', title: 'Mais vendas, maior margem', desc: 'Estratégias que geram leads qualificados e um processo de conversão que funciona mesmo no mês ruim.' },
  { icon: '⚙️', title: 'Processos otimizados', desc: 'Operação que roda sem improviso. Cada etapa mapeada, cada responsável definido, cada resultado rastreável.' },
  { icon: '📊', title: 'Controle e clareza', desc: 'Dados reais para decidir com segurança — sem achismo, sem planilha perdida, sem chute no escuro.' },
  { icon: '🏋️', title: 'Equipe de alta performance', desc: 'Time treinado, motivado e com metas individuais — que atende bem, defende a marca e fecha mais.' },
  { icon: '🗺️', title: 'Expansão planejada', desc: 'Crescimento com estratégia: domínio regional, expansão territorial e posicionamento de mercado consistente.' },
  { icon: '🕒', title: 'Previsibilidade e liberdade', desc: 'Você sabe aonde quer chegar. Nós conhecemos o caminho. Juntos alcançaremos resultados extraordinários.' },
]
</script>

<style scoped>
.res__grid { display: grid; grid-template-columns: repeat(3,1fr); gap: 14px; margin-top: 48px; }
.rcard { background: #fff; border: 1px solid var(--bdr); border-radius: 12px; padding: 24px; transition: all .25s; opacity: 0; transform: translateY(14px); }
.rcard.revealed { opacity: 1; transform: translateY(0); transition: opacity .5s ease, transform .5s ease; }
.rcard:hover { box-shadow: var(--sh2); transform: translateY(-3px); border-color: var(--bdr2); }
.rcard__ic { width: 44px; height: 44px; background: var(--gs); border-radius: 10px; display: flex; align-items: center; justify-content: center; font-size: 20px; margin-bottom: 16px; }
.rcard h3 { font-family: 'Space Grotesk', sans-serif; font-size: 15px; font-weight: 700; color: var(--ink); margin-bottom: 7px; }
.rcard p { font-size: 13px; color: var(--sub); line-height: 1.6; margin: 0; }
@media (max-width: 900px) { .res__grid { grid-template-columns: 1fr; } }
</style>
