<template>
  <section id="metodo" class="section section--white">
    <div class="container">
      <span class="tag">A metodologia CWA</span>
      <h2 class="title">O Método <em>N.I.T.R.O</em> — 5 etapas,<br/>6 meses, 1 operação previsível</h2>
      <p class="subtitle">Desenvolvido pela CWA para o mercado automotivo. Cada etapa tem entregáveis claros, responsáveis definidos e métricas acompanhadas de perto.</p>
      <div class="divider"></div>
      <div class="meth__layout">
        <!-- Steps -->
        <div class="meth__steps">
          <div v-for="step in steps" :key="step.letter" class="mstep reveal">
            <div class="mstep__letter">{{ step.letter }}</div>
            <div>
              <span class="mbadge">{{ step.badge }}</span>
              <h3>{{ step.title }}</h3>
              <p>{{ step.desc }}</p>
            </div>
          </div>
        </div>

        <!-- Timeline card -->
        <div class="tl-card">
          <img src="../../public/assets/img/logo.webp" alt="CWA Digital" class="tl-card__logo" />
          <h3>Sua jornada de transformação</h3>
          <p class="tl-card__desc">6 meses com entregáveis claros e acompanhamento próximo do time CWA.</p>
          <div class="tl-items">
            <div v-for="(tl, i) in timeline" :key="tl.letter" class="tli">
              <div class="tli__left">
                <div class="tli__dot">{{ tl.letter }}</div>
                <div v-if="i < timeline.length - 1" class="tli__line"></div>
              </div>
              <div>
                <div class="tli__month">{{ tl.month }}</div>
                <div class="tli__title">{{ tl.title }}</div>
                <div class="tli__desc">{{ tl.desc }}</div>
              </div>
            </div>
          </div>
          <div class="mq">
            <p>"Vender mais é questão de método. Não de sorte."</p>
            <span>— Método N.I.T.R.O · CWA Digital</span>
          </div>
        </div>
      </div>
    </div>
  </section>
</template>

<script setup>
import { useScrollReveal } from '@/composables/useScrollReveal'
useScrollReveal('.reveal')

const steps = [
  { letter: 'N', badge: 'Mês 1 · Tração e Direção', title: 'Diagnóstico, Setup e Arrancada', desc: 'Mapeamos toda a operação, definimos posicionamento, ativamos as primeiras campanhas e configuramos as ferramentas. O motor liga antes do mês acabar — sem enrolação.' },
  { letter: 'I', badge: 'Meses 2–3 · Inteligência', title: 'Processos, Dados e Desenvolvimento de Equipe', desc: 'Rotinas comerciais estruturadas, time treinado com PDI individual, OKRs definidos e automações de reativação de base. A operação começa a funcionar com método — não com sorte.' },
  { letter: 'T', badge: 'Mês 4 · Turbo', title: 'Aceleração Total do Funil', desc: 'Pipeline otimizado, modelo de vendedor líder implementado, campanhas de domínio territorial. Clientes satisfeitos se tornam embaixadores da sua marca.' },
  { letter: 'R', badge: 'Mês 5 · Radar', title: 'Domínio de Mercado', desc: 'Expansão territorial, inteligência de dados intensificada e parcerias regionais. Sua marca se consolida como referência da categoria na região.' },
  { letter: 'O', badge: 'Mês 6 · Otimização', title: 'Melhoria Contínua e Inovação', desc: 'Testes A/B, análise de ROI por canal, automações avançadas e planejamento preditivo 365 dias. Uma operação que nunca para de crescer.' },
]
const timeline = [
  { letter: 'N', month: 'Mês 1', title: 'Tração e Direção', desc: 'Briefing → Setup → Campanhas no ar' },
  { letter: 'I', month: 'Meses 2–3', title: 'Inteligência Operacional', desc: 'Processos → PDI → OKRs → Automações' },
  { letter: 'T', month: 'Mês 4', title: 'Turbo', desc: 'Pipeline → Vendedor líder → Domínio' },
  { letter: 'R', month: 'Mês 5', title: 'Radar de Mercado', desc: 'Expansão → Base fidelizada → Referência' },
  { letter: 'O', month: 'Mês 6', title: 'Otimização e Escala', desc: 'ROI → IA avançada → Plano 365 dias' },
]
</script>

<style scoped>
.meth__layout { display: grid; grid-template-columns: 1fr 1fr; gap: 64px; align-items: start; margin-top: 48px; }
.mstep { display: flex; gap: 16px; padding: 20px 0; border-bottom: 1px solid var(--bdr); opacity: 0; transform: translateY(16px); }
.mstep:first-child { padding-top: 0; }
.mstep.revealed { opacity: 1; transform: translateY(0); transition: opacity .55s ease, transform .55s ease; }
.mstep__letter { font-family: 'Space Grotesk', sans-serif; font-size: 44px; font-weight: 700; color: var(--g); line-height: 1; min-width: 32px; letter-spacing: -2px; }
.mbadge { display: inline-block; font-size: 10px; font-weight: 600; letter-spacing: 1.5px; text-transform: uppercase; color: var(--g); background: var(--gs); border: 1px solid var(--bdr2); padding: 3px 9px; border-radius: 100px; margin-bottom: 5px; }
.mstep h3 { font-family: 'Space Grotesk', sans-serif; font-size: 15px; font-weight: 600; color: var(--ink); margin-bottom: 4px; }
.mstep p { font-size: 13px; color: var(--sub); line-height: 1.6; margin: 0; }
/* Timeline */
.tl-card { background: #fff; border: 1px solid var(--bdr); border-radius: 14px; padding: 26px; position: sticky; top: 82px; box-shadow: var(--sh2); }
.tl-card__logo { height: 22px; object-fit: contain; margin-bottom: 16px; display: block; }
.tl-card h3 { font-family: 'Space Grotesk', sans-serif; font-size: 17px; font-weight: 700; color: var(--ink); margin-bottom: 4px; }
.tl-card__desc { font-size: 12px; color: var(--muted); margin-bottom: 20px; }
.tl-items { display: flex; flex-direction: column; }
.tli { display: flex; gap: 11px; padding: 10px 0; }
.tli__left { display: flex; flex-direction: column; align-items: center; }
.tli__dot { width: 30px; height: 30px; border-radius: 50%; background: var(--g); display: flex; align-items: center; justify-content: center; font-family: 'Space Grotesk', sans-serif; font-size: 13px; font-weight: 700; color: #fff; flex-shrink: 0; }
.tli__line { width: 2px; flex: 1; background: var(--bdr); margin: 3px 0; min-height: 12px; }
.tli__month { font-size: 10px; font-weight: 600; letter-spacing: 1.5px; text-transform: uppercase; color: var(--g); margin-bottom: 2px; }
.tli__title { font-size: 13px; font-weight: 600; color: var(--ink); font-family: 'Space Grotesk', sans-serif; }
.tli__desc { font-size: 11px; color: var(--muted); margin-top: 2px; line-height: 1.5; }
.mq { background: var(--gs); border: 1px solid var(--bdr2); border-radius: 9px; padding: 14px; margin-top: 16px; }
.mq p { font-size: 13px; color: var(--sub); font-style: italic; line-height: 1.6; margin: 0; }
.mq span { font-size: 10px; color: var(--g); font-weight: 700; letter-spacing: 1.5px; text-transform: uppercase; margin-top: 6px; display: block; }
@media (max-width: 900px) { .meth__layout { grid-template-columns: 1fr; } }
</style>
