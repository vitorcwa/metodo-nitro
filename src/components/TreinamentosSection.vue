<template>
  <section class="section section--gray">
    <div class="container">
      <span class="tag">Desenvolvimento completo</span>
      <h2 class="title">Treinamentos que <em>mudam o jogo</em><br/>da sua operação</h2>
      <p class="subtitle">Além do PDI individual, a CWA entrega trilhas de treinamento para cada função do time — com foco em conversão e resultado.</p>
      <div class="divider"></div>
      <div class="train__grid">
        <div v-for="t in treinamentos" :key="t.title" class="trcard reveal">
          <div class="trcard__ic">{{ t.icon }}</div>
          <h3>{{ t.title }}</h3>
          <p>{{ t.desc }}</p>
          <div class="trcard__tags">
            <span v-for="tag in t.tags" :key="tag">{{ tag }}</span>
          </div>
        </div>
      </div>
    </div>
  </section>
</template>

<script setup>
import { useScrollReveal } from '@/composables/useScrollReveal'
useScrollReveal('.reveal')

const treinamentos = [
  { icon: '🏎️', title: 'Alta Performance para Vendedores', desc: 'Técnicas de abordagem, negociação, gestão de objeções e fechamento. Vendedor que entende processo fecha mais, independente do mês.', tags: ['Negociação', 'Fechamento', 'Objeções'] },
  { icon: '📞', title: 'Pré-Vendas e Qualificação', desc: 'Protocolos de atendimento, scripts de qualificação e fluxo de agendamento. Pré-venda bem treinada multiplica as visitas presenciais.', tags: ['Scripts', 'Agendamento', 'Qualificação'] },
  { icon: '🔑', title: 'Consignação e Captação', desc: 'Técnicas específicas para consignadores: como captar, avaliar e negociar veículos com margem. Pátio cheio com estoque qualificado.', tags: ['Captação', 'Avaliação', 'Margem'] },
  { icon: '📹', title: 'Produção Audiovisual', desc: 'O time aprende a criar conteúdo automotivo de alta qualidade — reels, stories e vídeos que vendem dentro da loja e nas redes.', tags: ['Reels', 'Stories', 'Conteúdo'] },
  { icon: '⚙️', title: 'Gestão de Processos e Metodologia Ágil', desc: 'Gestores aprendem a usar dados e métricas para tomar decisões mais rápidas e assertivas. Operação inteligente e escalável.', tags: ['OKRs', 'Dados', 'Liderança'] },
  { icon: '🤖', title: 'Uso de Ferramentas e IA', desc: 'Time treinado no Garage HUB, automações e inteligência artificial aplicada ao processo de vendas. Tecnologia a favor de quem vende.', tags: ['Garage HUB', 'IA', 'Automação'] },
]
</script>

<style scoped>
.train__grid { display: grid; grid-template-columns: repeat(3,1fr); gap: 14px; margin-top: 48px; }
.trcard { background: #fff; border: 1px solid var(--bdr); border-radius: 12px; padding: 24px; transition: all .25s; position: relative; overflow: hidden; opacity: 0; transform: translateY(14px); }
.trcard.revealed { opacity: 1; transform: translateY(0); transition: opacity .5s ease, transform .5s ease; }
.trcard::after { content: ''; position: absolute; top: 0; left: 0; right: 0; height: 3px; background: var(--g); }
.trcard:hover { box-shadow: var(--sh2); transform: translateY(-3px); }
.trcard__ic { width: 44px; height: 44px; background: var(--gs); border-radius: 10px; display: flex; align-items: center; justify-content: center; font-size: 20px; margin-bottom: 16px; }
.trcard h3 { font-family: 'Space Grotesk', sans-serif; font-size: 15px; font-weight: 700; color: var(--ink); margin-bottom: 7px; }
.trcard p { font-size: 13px; color: var(--sub); line-height: 1.6; margin: 0; }
.trcard__tags { display: flex; flex-wrap: wrap; gap: 5px; margin-top: 12px; }
.trcard__tags span { font-size: 10px; font-weight: 600; padding: 3px 9px; border-radius: 100px; background: var(--bg); border: 1px solid var(--bdr); color: var(--muted); }
@media (max-width: 900px) { .train__grid { grid-template-columns: 1fr; } }
</style>
