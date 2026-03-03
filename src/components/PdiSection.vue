<template>
  <section id="pdi" class="section section--white">
    <div class="container">
      <span class="tag">Desenvolvimento de pessoas</span>
      <h2 class="title">PDI — Plano de Desenvolvimento<br/><em>Individual por Vendedor</em></h2>
      <p class="subtitle">Não treinamos em grupo e esquecemos. A CWA mapeia cada membro do time comercial e cria um plano de evolução personalizado — porque equipe forte fecha mais.</p>
      <div class="divider"></div>
      <div class="pdi__layout">

        <!-- Flowchart -->
        <div class="pdi__flow-wrap">
          <div class="pdi__flow-title">Fluxo do PDI CWA</div>
          <div class="pdi__flow-sub">Ciclo contínuo de diagnóstico, desenvolvimento e resultado</div>
          <div class="flowchart">
            <div class="fc-node fc-node--green">
              <div class="fc-node__title" style="color:var(--g)">🔍 Diagnóstico Individual</div>
              <div class="fc-node__sub">Análise de performance, pontos fortes e gaps de cada vendedor</div>
            </div>
            <div class="fc-arrow"><div class="fc-arrow__line"></div><div class="fc-arrow__head"></div></div>
            <div class="fc-node fc-node--gray">
              <div class="fc-node__title">📋 Plano Personalizado</div>
              <div class="fc-node__sub">Metas individuais, conteúdos e trilha de desenvolvimento sob medida</div>
            </div>
            <div class="fc-arrow"><div class="fc-arrow__line"></div><div class="fc-arrow__head"></div></div>
            <div class="fc-split">
              <div class="fc-split__line"></div>
              <span>Trilhas paralelas</span>
              <div class="fc-split__line"></div>
            </div>
            <div class="fc-row">
              <div class="fc-node fc-node--gray fc-node--sm">
                <div class="fc-node__title">🎓 Treinamento Técnico</div>
                <div class="fc-node__sub">Negociação, objeções, fechamento</div>
              </div>
              <div class="fc-node fc-node--gray fc-node--sm">
                <div class="fc-node__title">🧠 Comportamental</div>
                <div class="fc-node__sub">Comunicação, disciplina, mentalidade</div>
              </div>
            </div>
            <div class="fc-arrow" style="margin-top:4px"><div class="fc-arrow__line"></div><div class="fc-arrow__head"></div></div>
            <div class="fc-node fc-node--gray">
              <div class="fc-node__title">📊 Indicadores Monitorados Semanalmente</div>
              <div class="fc-node__sub">Métricas individuais acompanhadas pelo time CWA semana a semana</div>
            </div>
            <div class="fc-arrow"><div class="fc-arrow__line"></div><div class="fc-arrow__head"></div></div>
            <div class="fc-node fc-node--success">
              <div class="fc-node__title" style="color:#fff">🏆 Vendedor de Alta Performance</div>
              <div class="fc-node__sub" style="color:rgba(255,255,255,.8)">Consistente, autônomo e com metas batidas todo mês</div>
            </div>
            <div class="fc-arrow">
              <div class="fc-arrow__line" style="background:var(--bdr2)"></div>
              <div class="fc-arrow__head" style="border-top-color:var(--bdr2)"></div>
            </div>
            <div class="fc-node fc-node--loop">
              <div class="fc-node__title" style="color:var(--g);font-size:12px">🔄 Novo ciclo — revisão e evolução contínua</div>
            </div>
          </div>
        </div>

        <!-- Text + benefits -->
        <div class="pdi__content">
          <p class="pdi__lead">O PDI é uma das entregas mais valiosas do Método N.I.T.R.O. Enquanto a maioria das agências foca só em tráfego, <strong>a CWA cuida também de quem vai fechar a venda.</strong></p>
          <p class="pdi__body">Cada vendedor, pré-vendedor e consignador recebe um plano individual — com diagnóstico próprio, trilha de conteúdo personalizada e metas acompanhadas semana a semana pelo nosso time.</p>
          <div class="pdi__items">
            <div v-for="item in pdiItems" :key="item.title" class="pdi-item reveal">
              <div class="pdi-item__ic">{{ item.icon }}</div>
              <div>
                <h4>{{ item.title }}</h4>
                <p>{{ item.desc }}</p>
              </div>
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

const pdiItems = [
  { icon: '🔍', title: 'Diagnóstico individual profundo', desc: 'Avaliamos cada membro do time: taxa de conversão, abordagem, gestão de objeções e comportamentos que sabotam resultados.' },
  { icon: '🎯', title: 'Metas e trilha personalizadas', desc: 'Não existe receita de bolo. Cada pessoa tem seu plano — porque o que falta para um é diferente do que falta para o outro.' },
  { icon: '📊', title: 'Indicadores acompanhados semana a semana', desc: 'A CWA monitora a evolução individual e intervém quando necessário. O time cresce junto com a operação.' },
  { icon: '🔄', title: 'Ciclo contínuo — sem estagnação', desc: 'A cada ciclo completado, o PDI é revisado e evoluído. O desenvolvimento do time nunca para — assim como os seus resultados.' },
]
</script>

<style scoped>
.pdi__layout { display: grid; grid-template-columns: 1fr 1fr; gap: 72px; align-items: center; margin-top: 48px; }
/* Flowchart */
.pdi__flow-wrap { background: #fff; border: 1px solid var(--bdr); border-radius: 14px; padding: 24px; box-shadow: var(--sh2); }
.pdi__flow-title { font-family: 'Space Grotesk', sans-serif; font-size: 14px; font-weight: 700; color: var(--ink); margin-bottom: 4px; }
.pdi__flow-sub { font-size: 12px; color: var(--muted); margin-bottom: 20px; }
.flowchart { display: flex; flex-direction: column; align-items: center; }
.fc-node { width: 100%; border-radius: 9px; padding: 12px 14px; text-align: center; }
.fc-node--green { background: var(--gs); border: 1.5px solid var(--bdr2); }
.fc-node--gray { background: var(--bg2); border: 1px solid var(--bdr); }
.fc-node--success { background: linear-gradient(135deg, #18B25A, #34D680); border: none; }
.fc-node--loop { background: var(--gs); border: 1px dashed var(--bdr2); opacity: .8; }
.fc-node--sm .fc-node__title { font-size: 12px; }
.fc-node__title { font-family: 'Space Grotesk', sans-serif; font-size: 13px; font-weight: 700; color: var(--ink); }
.fc-node__sub { font-size: 11px; margin-top: 2px; line-height: 1.4; color: var(--sub); }
.fc-arrow { display: flex; flex-direction: column; align-items: center; padding: 3px 0; }
.fc-arrow__line { width: 2px; height: 16px; background: var(--bdr); }
.fc-arrow__head { width: 0; height: 0; border-left: 5px solid transparent; border-right: 5px solid transparent; border-top: 6px solid var(--bdr); }
.fc-row { display: grid; grid-template-columns: 1fr 1fr; gap: 7px; width: 100%; margin-top: 4px; }
.fc-split { display: flex; align-items: center; gap: 7px; padding: 3px 0; width: 100%; }
.fc-split__line { flex: 1; height: 1.5px; background: var(--bdr); }
.fc-split span { font-size: 10px; font-weight: 600; color: var(--muted); white-space: nowrap; }
/* Content */
.pdi__lead { font-size: 17px; color: var(--sub); line-height: 1.8; margin-bottom: 16px; }
.pdi__lead strong { color: var(--ink); }
.pdi__body { font-size: 15px; color: var(--sub); line-height: 1.8; margin-bottom: 28px; }
.pdi__items { display: flex; flex-direction: column; gap: 14px; }
.pdi-item { display: flex; gap: 13px; align-items: flex-start; opacity: 0; transform: translateY(14px); }
.pdi-item.revealed { opacity: 1; transform: translateY(0); transition: opacity .5s ease, transform .5s ease; }
.pdi-item__ic { width: 34px; height: 34px; min-width: 34px; background: var(--gs); border: 1px solid var(--bdr2); border-radius: 8px; display: flex; align-items: center; justify-content: center; font-size: 15px; }
.pdi-item h4 { font-family: 'Space Grotesk', sans-serif; font-size: 14px; font-weight: 600; color: var(--ink); margin-bottom: 3px; }
.pdi-item p { font-size: 13px; color: var(--sub); line-height: 1.6; margin: 0; }
@media (max-width: 900px) { .pdi__layout { grid-template-columns: 1fr; } }
</style>
