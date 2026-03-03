<template>
  <section id="solucoes" class="section section--dark funil-sec">
    <div class="container">
      <span class="tag tag--dark">Tecnologia dentro do Método N.I.T.R.O</span>
      <h2 class="funil-sec__title title">
        O Garage HUB é a ferramenta que<br/>
        <em>potencializa cada etapa da operação</em>
      </h2>
      <p class="funil-sec__sub">Desenvolvido pela CWA para o automotivo. Uma ferramenta dentro do método — não o método em si. Automatiza e conecta todo o processo comercial, de ponta a ponta.</p>
      <div class="divider divider--light"></div>
      <div class="funil__layout">
        <!-- Flows list -->
        <div class="faflows">
          <div v-for="flow in flows" :key="flow.label" class="faflow reveal">
            <div class="faflow__dot"></div>
            <p>{{ flow.label }}</p>
            <span>{{ flow.badge }}</span>
          </div>
        </div>

        <!-- Funil visual -->
        <div class="funil-card">
          <div class="funil-card__hdr">
            <img src="../../public/assets/img/logo-cwa.webp" alt="CWA" />
            <div>
              <div class="funil-card__title">Fluxo automatizado — Garage HUB</div>
              <div class="funil-card__sub">Do lead ao embaixador em etapas inteligentes</div>
            </div>
          </div>
          <div class="fsteps">
            <template v-for="(step, i) in fsteps" :key="step.label">
              <div class="fstep" :class="`fstep--${step.variant}`">
                <span class="fstep__ic">{{ step.icon }}</span>
                <div>
                  <div class="fstep__title">{{ step.label }}</div>
                  <div class="fstep__sub">{{ step.sub }}</div>
                </div>
                <span class="fstep__badge">{{ step.badge }}</span>
              </div>
              <div v-if="i < fsteps.length - 1" class="farrow">↓</div>
            </template>
          </div>
        </div>
      </div>
    </div>
  </section>
</template>

<script setup>
import { useScrollReveal } from '@/composables/useScrollReveal'
useScrollReveal('.reveal')

const flows = [
  { label: 'Pré-atendimento e qualificação automática de leads', badge: '⚡ Segundos' },
  { label: 'Confirmação e reagendamento automático de test-drives', badge: '🗓️ 24/7' },
  { label: 'Follow-up segmentado por status de CPF aprovado/reprovado', badge: '🎯 Inteligente' },
  { label: 'Reativação de leads após 30, 60 e 90 dias de inatividade', badge: '🔁 Automático' },
  { label: 'Pesquisa pós-venda e geração de avaliações 5 estrelas', badge: '⭐ Reputação' },
  { label: 'Resposta automática a comentários e DMs no Instagram', badge: '💬 Imediato' },
  { label: 'Campanhas de indicação e recompra ativadas por dados', badge: '💰 Receita' },
  { label: 'Ativação de feirões e eventos de venda em massa', badge: '🚀 Escala' },
]
const fsteps = [
  { icon: '📥', label: 'Lead chega', sub: 'Meta · Google · Instagram · TikTok', badge: 'Entrada', variant: 'entry' },
  { icon: '⚡', label: 'Garage HUB ativa', sub: 'Responde em segundos · Qualifica automaticamente', badge: 'Imediato', variant: 'active' },
  { icon: '📅', label: 'Agendamento', sub: 'Test-drive confirmado · Follow-up ativo', badge: 'Engajado', variant: 'neutral' },
  { icon: '🤝', label: 'Visita presencial', sub: '25% dos agendados chegam à loja', badge: 'Na loja', variant: 'neutral' },
  { icon: '✅', label: 'Venda + Embaixador', sub: 'Pós-venda automático · Indicação ativada', badge: 'Convertido', variant: 'success' },
]
</script>

<style scoped>
.funil-sec { position: relative; overflow: hidden; }
.funil-sec::before { content: ''; position: absolute; top: 0; right: 0; width: 500px; height: 500px; border-radius: 50%; background: radial-gradient(circle, rgba(24,178,90,.06), transparent 65%); }
.funil-sec__title { color: #fff; font-size: clamp(30px, 3.8vw, 46px); }
.funil-sec__title em { color: #34D680; }
.funil-sec__sub { font-size: 16px; color: rgba(255,255,255,.45); margin-top: 14px; max-width: 540px; line-height: 1.75; }
.funil__layout { display: grid; grid-template-columns: 1fr 1fr; gap: 72px; align-items: start; margin-top: 48px; }
.faflows { display: flex; flex-direction: column; gap: 7px; }
.faflow { background: rgba(255,255,255,.04); border: 1px solid rgba(255,255,255,.07); border-radius: 9px; padding: 12px 15px; display: flex; align-items: center; gap: 11px; transition: all .2s; opacity: 0; transform: translateY(14px); }
.faflow.revealed { opacity: 1; transform: translateY(0); transition: opacity .5s ease, transform .5s ease; }
.faflow:hover { border-color: rgba(24,178,90,.3); background: rgba(24,178,90,.05); }
.faflow__dot { width: 6px; height: 6px; border-radius: 50%; background: var(--g); flex-shrink: 0; }
.faflow p { font-size: 13px; color: rgba(255,255,255,.65); font-weight: 500; margin: 0; flex: 1; }
.faflow span { font-size: 10px; font-weight: 700; background: rgba(24,178,90,.12); border: 1px solid rgba(24,178,90,.25); color: #34D680; padding: 3px 9px; border-radius: 100px; white-space: nowrap; }
/* Funil card */
.funil-card { background: rgba(255,255,255,.04); border: 1px solid rgba(255,255,255,.08); border-radius: 14px; padding: 24px; }
.funil-card__hdr { display: flex; align-items: center; gap: 9px; margin-bottom: 20px; padding-bottom: 14px; border-bottom: 1px solid rgba(255,255,255,.07); }
.funil-card__hdr img { height: 18px; object-fit: contain; }
.funil-card__title { font-size: 12px; font-weight: 600; color: rgba(255,255,255,.8); }
.funil-card__sub { font-size: 10px; color: rgba(255,255,255,.35); margin-top: 2px; }
.fsteps { display: flex; flex-direction: column; gap: 5px; }
.fstep { border-radius: 8px; padding: 12px 14px; display: flex; align-items: center; gap: 9px; }
.fstep__ic { font-size: 14px; min-width: 16px; }
.fstep__title { font-size: 12px; font-weight: 600; }
.fstep__sub { font-size: 10px; margin-top: 1px; opacity: .65; }
.fstep__badge { font-size: 10px; font-weight: 700; padding: 3px 9px; border-radius: 100px; margin-left: auto; white-space: nowrap; }
.fstep--entry { background: rgba(24,178,90,.1); border: 1px solid rgba(24,178,90,.2); }
.fstep--entry .fstep__title { color: rgba(255,255,255,.9); }
.fstep--entry .fstep__badge { background: rgba(24,178,90,.15); color: #34D680; }
.fstep--active { background: rgba(24,178,90,.15); border: 1px solid rgba(24,178,90,.3); }
.fstep--active .fstep__title { color: #fff; }
.fstep--active .fstep__badge { background: rgba(24,178,90,.2); color: #34D680; }
.fstep--neutral { background: rgba(255,255,255,.04); border: 1px solid rgba(255,255,255,.07); }
.fstep--neutral .fstep__title { color: rgba(255,255,255,.85); }
.fstep--neutral .fstep__badge { background: rgba(255,255,255,.06); color: rgba(255,255,255,.5); }
.fstep--success { background: linear-gradient(135deg, #18B25A, #34D680); border: none; }
.fstep--success .fstep__title { color: #fff; }
.fstep--success .fstep__sub { color: rgba(255,255,255,.75); opacity: 1; }
.fstep--success .fstep__badge { background: rgba(255,255,255,.2); color: #fff; }
.farrow { text-align: center; color: rgba(255,255,255,.18); font-size: 13px; padding: 1px 0; line-height: 1; }
@media (max-width: 900px) { .funil__layout { grid-template-columns: 1fr; } }
</style>
