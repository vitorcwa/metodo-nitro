<template>
  <section class="hero">
    <div class="hero__dots"></div>
    <div class="hero__orb"></div>
    <div class="container">
      <div class="hero__layout">
        <!-- LEFT -->
        <div class="hero__content">
          <div class="hero__eyebrow fade-up">
            <div class="hero__dots-row">
              <i style="background:var(--g)"></i>
              <i style="background:var(--pk)"></i>
              <i style="background:var(--ink)"></i>
            </div>
            <span>8+ anos no mercado automotivo · Todo o Brasil</span>
          </div>
          <h1 class="fade-up delay-1">
            Sua multimarcas<br />pronta para
            <em>escalar<br />de verdade.</em>
          </h1>
          <p class="hero__sub fade-up delay-2">
            A CWA une <strong>estratégia, tecnologia e desenvolvimento de equipe</strong>
            para transformar multimarcas e concessionárias em operações previsíveis,
            lucrativas e dominantes na sua região.
          </p>
          <div class="hero__btns fade-up delay-3">
            <a href="#diagnostico" class="btn btn--green">🔥 Quero meu diagnóstico gratuito →</a>
            <a href="#metodo" class="btn btn--outline">Ver o Método N.I.T.R.O</a>
          </div>
          <p class="hero__fine fade-up delay-4">Sem compromisso · 100% gratuito · Resposta em até 24h</p>
          <div class="hero__stats fade-up delay-4">
            <div v-for="stat in stats" :key="stat.label" class="hstat">
              <div class="hstat__n">{{ stat.value }}<em>{{ stat.suffix }}</em></div>
              <div class="hstat__l" v-html="stat.label"></div>
            </div>
          </div>
        </div>

        <!-- RIGHT — Dashboard -->
        <div class="hero__visual fade-up delay-2">
          <div class="hcard float-anim">
            <div class="hcard__bar">
              <span class="hbar-dot" style="background:#ff5f57"></span>
              <span class="hbar-dot" style="background:#ffbd2e"></span>
              <span class="hbar-dot" style="background:#28ca41"></span>
              <span class="hbar__title">CWA · Painel da operação</span>
            </div>
            <div class="hcard__body">
              <div class="hkpis">
                <div v-for="kpi in kpis" :key="kpi.label" class="hkpi">
                  <div class="hkpi__v" :style="kpi.small ? 'font-size:16px' : ''">
                    {{ kpi.value }}<em>{{ kpi.suffix }}</em>
                  </div>
                  <div class="hkpi__l">{{ kpi.label }}</div>
                  <div class="hkpi__d">{{ kpi.delta }}</div>
                </div>
              </div>
              <div class="hchart">
                <div class="hchart__label">Leads por semana — crescimento com método</div>
                <div class="bars">
                  <div v-for="(b, i) in bars" :key="i" class="bar" :style="{ height: b.h, background: b.c }"></div>
                </div>
              </div>
              <div class="hleads">
                <div v-for="lead in leads" :key="lead.name" class="hlead">
                  <div class="hlead__av" :style="{ background: lead.color }">{{ lead.initials }}</div>
                  <div>
                    <div class="hlead__name">{{ lead.name }}</div>
                    <div class="hlead__status" :style="{ color: lead.statusColor }">{{ lead.status }}</div>
                  </div>
                </div>
              </div>
            </div>
          </div>
          <div class="fbadge fbadge--top">⚡ Automação ativa 24/7</div>
          <div class="fbadge fbadge--bot">🤖 IA tratando leads agora</div>
        </div>
      </div>
    </div>
  </section>
</template>

<script setup>
const stats = [
  { value: '8', suffix: '+', label: 'Anos no<br/>automotivo' },
  { value: '85', suffix: '%', label: 'Processo<br/>automatizado' },
  { value: '35', suffix: '%', label: 'Leads inativos<br/>reativados' },
  { value: '25', suffix: '%', label: 'Agendamentos<br/>→ visitas' },
]
const kpis = [
  { value: '142', suffix: '↑', label: 'Leads / mês', delta: '+38% vs ant.' },
  { value: '37', suffix: '%', label: 'Conversão', delta: '+12pts da meta' },
  { value: 'R$284k', suffix: '', label: 'Receita', delta: 'Meta batida ✓', small: true },
]
const bars = [
  { h: '26%', c: '#E4EDE8' }, { h: '40%', c: '#C8DDD2' }, { h: '34%', c: '#E4EDE8' },
  { h: '50%', c: '#A8CCBA' }, { h: '56%', c: '#C8DDD2' }, { h: '70%', c: '#18B25A' },
  { h: '60%', c: '#A8CCBA' }, { h: '86%', c: '#18B25A' }, { h: '100%', c: '#18B25A' },
]
const leads = [
  { initials: 'JM', name: 'João Mendes', status: '● Test-drive agendado', color: '#18B25A', statusColor: '#18B25A' },
  { initials: 'AC', name: 'Ana Costa', status: '● Follow-up ativo', color: '#5A7A8A', statusColor: '#F5A623' },
  { initials: 'RP', name: 'Rafael P.', status: '● Proposta enviada', color: '#12904A', statusColor: '#8AADA0' },
  { initials: 'ML', name: 'Marcos L.', status: '● Venda fechada ✓', color: '#0D1F17', statusColor: '#18B25A' },
]
</script>

<style scoped>
.hero {
  min-height: 100vh; display: flex; align-items: center;
  padding: 112px 0 80px; position: relative; overflow: hidden;
  background: linear-gradient(158deg, #F4F9F6 0%, #ECF5EF 55%, #E6F2EA 100%);
}
.hero__dots {
  position: absolute; inset: 0;
  background-image: radial-gradient(circle, rgba(24,178,90,.12) 1px, transparent 1px);
  background-size: 32px 32px;
  mask-image: radial-gradient(ellipse 80% 80% at 65% 45%, black, transparent);
}
.hero__orb {
  position: absolute; top: -80px; right: -80px; width: 580px; height: 580px;
  border-radius: 50%; background: radial-gradient(circle, rgba(24,178,90,.07) 0%, transparent 65%);
}
.hero__layout {
  position: relative; z-index: 2;
  display: grid; grid-template-columns: 1.05fr .95fr; gap: 64px; align-items: center;
}
.hero__eyebrow { display: flex; align-items: center; gap: 10px; margin-bottom: 22px; }
.hero__dots-row { display: flex; gap: 5px; }
.hero__dots-row i { display: block; width: 8px; height: 8px; border-radius: 50%; }
.hero__eyebrow span { font-size: 12px; font-weight: 600; letter-spacing: 2px; text-transform: uppercase; color: var(--g); }
h1 { font-size: clamp(42px, 5.2vw, 66px); color: var(--ink); letter-spacing: -1.5px; margin-bottom: 0; }
h1 em { color: var(--g); font-style: normal; }
.hero__sub { font-size: 18px; color: var(--sub); margin: 18px 0 32px; max-width: 500px; line-height: 1.75; }
.hero__sub strong { color: var(--ink); }
.hero__btns { display: flex; gap: 12px; flex-wrap: wrap; }
.hero__fine {
  font-size: 12px; color: var(--muted); margin-top: 12px;
  display: flex; align-items: center; gap: 6px;
}
.hero__fine::before { content: ''; width: 4px; height: 4px; border-radius: 50%; background: var(--g); }
.hero__stats { display: flex; margin-top: 46px; padding-top: 30px; border-top: 1px solid var(--bdr); }
.hstat { padding-right: 28px; margin-right: 28px; border-right: 1px solid var(--bdr); }
.hstat:last-child { border-right: none; padding-right: 0; margin-right: 0; }
.hstat__n { font-family: 'Space Grotesk', sans-serif; font-size: 38px; font-weight: 700; color: var(--ink); letter-spacing: -2px; line-height: 1; }
.hstat__n em { color: var(--g); font-style: normal; }
.hstat__l { font-size: 12px; color: var(--muted); margin-top: 4px; line-height: 1.4; }

/* Dashboard */
.hero__visual { position: relative; }
.hcard { background: #fff; border: 1px solid var(--bdr); border-radius: 14px; box-shadow: var(--sh2); overflow: hidden; }
.hcard__bar { background: var(--bg2); border-bottom: 1px solid var(--bdr); padding: 11px 15px; display: flex; align-items: center; gap: 6px; }
.hbar-dot { width: 9px; height: 9px; border-radius: 50%; display: inline-block; }
.hbar__title { font-size: 11px; font-weight: 500; color: var(--muted); letter-spacing: .6px; margin-left: 6px; }
.hcard__body { padding: 16px; }
.hkpis { display: grid; grid-template-columns: repeat(3, 1fr); gap: 9px; margin-bottom: 12px; }
.hkpi { background: var(--bg); border: 1px solid var(--bdr); border-radius: 9px; padding: 12px; }
.hkpi__v { font-family: 'Space Grotesk', sans-serif; font-size: 20px; font-weight: 700; color: var(--ink); line-height: 1; }
.hkpi__v em { color: var(--g); font-style: normal; }
.hkpi__l { font-size: 9px; font-weight: 600; color: var(--muted); text-transform: uppercase; letter-spacing: 1px; margin-top: 2px; }
.hkpi__d { font-size: 10px; color: var(--g); font-weight: 600; margin-top: 3px; }
.hchart { background: var(--bg); border: 1px solid var(--bdr); border-radius: 9px; padding: 12px; margin-bottom: 11px; }
.hchart__label { font-size: 9px; font-weight: 600; color: var(--muted); text-transform: uppercase; letter-spacing: 1px; margin-bottom: 9px; }
.bars { display: flex; align-items: flex-end; gap: 4px; height: 50px; }
.bar { flex: 1; border-radius: 3px 3px 0 0; }
.hleads { display: grid; grid-template-columns: 1fr 1fr; gap: 7px; }
.hlead { background: var(--bg); border: 1px solid var(--bdr); border-radius: 7px; padding: 8px 10px; display: flex; align-items: center; gap: 7px; }
.hlead__av { width: 24px; height: 24px; border-radius: 50%; display: flex; align-items: center; justify-content: center; font-size: 8px; font-weight: 700; color: #fff; flex-shrink: 0; }
.hlead__name { font-size: 10px; font-weight: 600; color: var(--ink); }
.hlead__status { font-size: 9px; font-weight: 500; margin-top: 1px; }
.fbadge { position: absolute; font-size: 11px; font-weight: 600; padding: 7px 14px; border-radius: 100px; white-space: nowrap; box-shadow: var(--sh2); }
.fbadge--top { top: -13px; right: -11px; background: var(--g); color: #fff; }
.fbadge--bot { bottom: -11px; left: -11px; background: #fff; border: 1px solid var(--bdr); color: var(--ink); }

@media (max-width: 900px) {
  .hero__layout { grid-template-columns: 1fr; }
  .hero__visual { display: none; }
  .hero__stats { flex-wrap: wrap; gap: 16px; }
  .hstat { border-right: none; padding: 0; margin: 0; }
}
</style>
