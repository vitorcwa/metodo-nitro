<template>
  <section id="plano" class="section section--gray">
    <div class="container">
      <span class="tag">O nosso plano</span>
      <h2 class="title">Tudo que você precisa.<br/><em>Em um único parceiro.</em></h2>
      <p class="subtitle">Sem módulo avulso. Sem plano básico. Resultado de verdade não cabe em metade.</p>
      <div class="divider"></div>
      <div class="plan__layout">
        <!-- Card -->
        <div class="plan-card">
          <div class="plan-card__top">
            <div class="plan-card__tag">✦ Plano Único CWA · Método N.I.T.R.O ✦</div>
            <div class="plan-card__name">Plano Completo CWA</div>
            <div class="plan-card__sub">Contrato inicial de 6 meses · Tudo incluso abaixo</div>
          </div>
          <div class="plan-card__body">
            <div class="plan-its">
              <div v-for="item in planItems" :key="item" class="pit">{{ item }}</div>
            </div>
            <a href="#diagnostico" class="btn btn--green btn--full btn--lg">🔥 Quero acelerar meus resultados agora →</a>
            <p class="plan-card__fine">Diagnóstico gratuito antes de qualquer compromisso</p>
          </div>
        </div>
        <!-- Infos -->
        <div class="plan__infos">
          <div v-for="info in planInfos" :key="info.title" class="pinfo reveal">
            <h4>{{ info.title }}</h4>
            <p v-html="info.desc"></p>
          </div>
        </div>
      </div>
    </div>
  </section>
</template>

<script setup>
import { useScrollReveal } from '@/composables/useScrollReveal'
useScrollReveal('.reveal')

const planItems = [
  'Consultoria estratégica e de posicionamento',
  'Gestão de tráfego pago (Meta Ads, Google Ads e TikTok)',
  'Gestão de redes sociais e linha editorial estratégica',
  'Produção e edição de até 3 reels por semana',
  'Implementação e operação do Garage HUB CRM (ferramenta CWA)',
  'Automações estratégicas personalizadas rodando 24/7',
  'Treinamento de pré-vendas, consignadores e vendedores',
  'Treinamento de alta performance para o time comercial',
  'PDI individual para cada membro do time',
  'Treinamento de produção audiovisual',
  'Desenvolvimento de site integrado ao sistema de gestão',
  'Consultoria recorrente + suporte ativo via WhatsApp',
  'OKRs, relatórios de performance e plano preditivo 365 dias',
]
const planInfos = [
  { title: '🤝 Parceiro ativo, não fornecedor', desc: 'Batalharemos juntos nas trincheiras. A CWA acompanha indicadores, intervém quando necessário e evolui a estratégia junto com você mês a mês — sem sumir após a venda.' },
  { title: '🚀 Motor ligado já na 1ª semana', desc: 'A estratégia de arrancada (Quick Win) entra em execução imediata. Campanha no ar e processo rodando antes do mês acabar.' },
  { title: '📅 Onboarding em 15 dias, sem atropelos', desc: 'Briefing → Kickoff → Mapa operacional → Setup → Treinamento. Cada etapa tem data, dono e entregável claro. Sem promessa vaga.' },
  { title: '📍 Para quem é esse plano?', desc: 'Para multimarcas e concessionárias que já vendem, mas sabem que estão deixando receita na mesa. <strong>Você sabe aonde quer chegar. Nós conhecemos o caminho.</strong>' },
]
</script>

<style scoped>
.plan__layout { display: grid; grid-template-columns: 1fr 1.1fr; gap: 44px; align-items: start; margin-top: 48px; }
.plan-card { background: #fff; border: 1.5px solid var(--g); border-radius: 14px; overflow: hidden; box-shadow: 0 0 0 4px rgba(24,178,90,.05), var(--sh2); }
.plan-card__top { background: linear-gradient(135deg, #18B25A, #34D680); padding: 24px 28px; }
.plan-card__tag { font-size: 10px; font-weight: 700; letter-spacing: 2px; text-transform: uppercase; color: rgba(255,255,255,.6); margin-bottom: 5px; }
.plan-card__name { font-family: 'Space Grotesk', sans-serif; font-size: 22px; font-weight: 700; color: #fff; }
.plan-card__sub { font-size: 12px; color: rgba(255,255,255,.7); margin-top: 4px; }
.plan-card__body { padding: 24px 28px; }
.plan-its { display: flex; flex-direction: column; gap: 8px; margin-bottom: 22px; }
.pit { display: flex; gap: 9px; font-size: 13px; color: var(--sub); }
.pit::before { content: '✓'; color: var(--g); font-weight: 700; min-width: 13px; font-size: 13px; }
.btn--lg { font-size: 15px; padding: 16px; }
.plan-card__fine { font-size: 12px; color: var(--muted); text-align: center; margin-top: 10px; }
.plan__infos { display: flex; flex-direction: column; gap: 11px; }
.pinfo { background: #fff; border: 1px solid var(--bdr); border-radius: 11px; padding: 16px 18px; opacity: 0; transform: translateY(14px); }
.pinfo.revealed { opacity: 1; transform: translateY(0); transition: opacity .5s ease, transform .5s ease; }
.pinfo h4 { font-family: 'Space Grotesk', sans-serif; font-size: 14px; font-weight: 700; color: var(--ink); margin-bottom: 4px; }
.pinfo p { font-size: 13px; color: var(--sub); line-height: 1.6; margin: 0; }
.pinfo :deep(strong) { color: var(--ink); }
@media (max-width: 900px) { .plan__layout { grid-template-columns: 1fr; } }
</style>
