<template>
  <section class="section section--gray">
    <div class="container">
      <span class="tag">Nós entendemos sua realidade</span>
      <h2 class="title">Respiramos o seu mercado<br/>e sabemos bem que<em>...</em></h2>
      <div class="divider"></div>
      <div class="prob__layout">
        <div class="prob__list">
          <div v-for="p in problemas" :key="p.title" class="pcard reveal">
            <div class="pcard__ic">{{ p.icon }}</div>
            <div>
              <h3>{{ p.title }}</h3>
              <p>{{ p.desc }}</p>
            </div>
          </div>
        </div>
        <div class="prob__right">
          <div class="pk-card">
            <p>"O Mercado está em crise para os que não se preparam, não se adaptam e os que se engessam em velhas práticas... <strong>Mas eu sei que, se você está aqui, esse não é o seu caso.</strong>"</p>
            <div class="pk-src">— CWA Digital</div>
          </div>
          <div class="pstats">
            <div v-for="s in pstats" :key="s.label" class="ps reveal">
              <div class="ps__n">{{ s.value }}<em>{{ s.suffix }}</em></div>
              <div class="ps__l">{{ s.label }}</div>
            </div>
          </div>
        </div>
      </div>
    </div>
  </section>
</template>

<script setup>
import { onMounted } from 'vue'
import { useScrollReveal } from '@/composables/useScrollReveal'
useScrollReveal('.reveal')

const problemas = [
  { icon: '🚗', title: 'Pátio vazio ou pátio lotado', desc: 'Hora falta carro, hora falta cliente. Sem previsibilidade, você apaga fogo em vez de construir crescimento.' },
  { icon: '💸', title: 'Anúncios caros, leads perdidos', desc: 'Você investe em tráfego, o lead chega e some. Sem processo estruturado, a concorrência fecha o que deveria ser sua venda.' },
  { icon: '⏱️', title: 'Processos lentos e ineficientes', desc: 'Planilha, papel e WhatsApp solto. Sem sistema, cada venda depende do talento individual — e isso não escala.' },
  { icon: '📊', title: 'Falta de clareza para decidir', desc: 'Sem dados confiáveis, toda decisão vira chute. Você corta o que gera resultado e repete o que não funciona.' },
  { icon: '😤', title: 'Trabalha muito, sente que não sai do lugar', desc: 'A frustração de dar o máximo e ver os números estagnados. Não é falta de esforço — é falta de método.' },
]
const pstats = [
  { value: '85', suffix: '%', label: 'do processo comercial pode ser automatizado' },
  { value: '35', suffix: '%', label: 'dos leads inativos reativados com fluxo estratégico' },
  { value: '25', suffix: '%', label: 'dos agendamentos viram visita presencial' },
  { value: '8',  suffix: '+', label: 'anos exclusivamente no setor automotivo' },
]
</script>

<style scoped>
.prob__layout { display: grid; grid-template-columns: 1fr 1fr; gap: 64px; align-items: start; margin-top: 48px; }
.prob__list { display: flex; flex-direction: column; gap: 9px; }
.pcard { background: #fff; border: 1px solid var(--bdr); border-radius: 11px; padding: 18px 20px; display: flex; gap: 13px; align-items: flex-start; position: relative; overflow: hidden; transition: all .2s; opacity: 0; transform: translateY(16px); }
.pcard.revealed { opacity: 1; transform: translateY(0); transition: opacity .55s ease, transform .55s ease; }
.pcard:hover { border-color: var(--bdr2); box-shadow: var(--sh); }
.pcard::before { content: ''; position: absolute; left: 0; top: 0; bottom: 0; width: 3px; background: var(--g); }
.pcard__ic { width: 36px; height: 36px; min-width: 36px; background: var(--gs); border-radius: 8px; display: flex; align-items: center; justify-content: center; font-size: 16px; }
.pcard h3 { font-family: 'Space Grotesk', sans-serif; font-size: 14px; font-weight: 600; color: var(--ink); margin-bottom: 3px; }
.pcard p { font-size: 13px; color: var(--sub); line-height: 1.6; margin: 0; }
.prob__right { display: flex; flex-direction: column; gap: 12px; }
.pk-card { background: linear-gradient(135deg, var(--pk) 0%, #9C0A38 100%); border-radius: 14px; padding: 28px; }
.pk-card p { font-size: 17px; font-weight: 500; color: rgba(255,255,255,.93); line-height: 1.65; font-style: italic; margin: 0; }
.pk-card p strong { color: #fff; font-style: normal; font-weight: 700; }
.pk-src { font-size: 10px; color: rgba(255,255,255,.4); font-weight: 600; letter-spacing: 2px; text-transform: uppercase; margin-top: 16px; }
.pstats { display: grid; grid-template-columns: 1fr 1fr; gap: 9px; }
.ps { background: #fff; border: 1px solid var(--bdr); border-radius: 10px; padding: 16px; text-align: center; opacity: 0; transform: translateY(16px); }
.ps.revealed { opacity: 1; transform: translateY(0); transition: opacity .55s ease, transform .55s ease; }
.ps__n { font-family: 'Space Grotesk', sans-serif; font-size: 32px; font-weight: 700; color: var(--ink); letter-spacing: -1px; line-height: 1; }
.ps__n em { color: var(--g); font-style: normal; }
.ps__l { font-size: 11px; color: var(--muted); margin-top: 4px; line-height: 1.4; }
@media (max-width: 900px) { .prob__layout { grid-template-columns: 1fr; } }
</style>
