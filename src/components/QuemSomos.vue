<template>
  <section id="quem" class="section section--white">
    <div class="container">
      <span class="tag">Prazer, somos a CWA</span>
      <h2 class="title">
        Um time de especialistas em<br />
        <em>alavancar negócios automotivos</em><br />
        através do digital.
      </h2>
      <div class="divider"></div>
      <div class="quem__layout">
        <div class="quem__text">
          <p>Atuamos há <strong>mais de 8 anos</strong> desenvolvendo projetos de marketing, comunicação e processos para Concessionárias, Locadoras, Proteções Veiculares e Auto Centers em todo o Brasil.</p>
          <p>Entendemos que cada cliente nos entrega bem mais que uma conta — também seus planos, sonhos e a projeção de um futuro repleto de sucesso. É com essa mentalidade que entregamos nossa máxima energia em cada projeto.</p>
          <p>Se você quer um time que não apenas conhece o seu mercado, mas que <strong>respira e vive os seus desafios</strong> e fala exatamente a sua língua… Prazer! Nós somos a CWA. <strong>A sua agência.</strong></p>
          <div class="pilares">
            <div v-for="p in pilares" :key="p.title" class="pilar">
              <div class="pilar__icon">{{ p.icon }}</div>
              <h4>{{ p.title }}</h4>
              <p>{{ p.desc }}</p>
            </div>
          </div>
        </div>
        <div class="quem__visual">
          <div class="map-wrap">
            <svg viewBox="0 0 400 348" fill="none" xmlns="http://www.w3.org/2000/svg">
              <rect width="400" height="348" fill="#F4F9F6"/>
              <line x1="0" y1="87" x2="400" y2="87" stroke="#DDE9E3" stroke-width="1"/>
              <line x1="0" y1="174" x2="400" y2="174" stroke="#DDE9E3" stroke-width="1"/>
              <line x1="0" y1="261" x2="400" y2="261" stroke="#DDE9E3" stroke-width="1"/>
              <line x1="100" y1="0" x2="100" y2="348" stroke="#DDE9E3" stroke-width="1"/>
              <line x1="200" y1="0" x2="200" y2="348" stroke="#DDE9E3" stroke-width="1"/>
              <line x1="300" y1="0" x2="300" y2="348" stroke="#DDE9E3" stroke-width="1"/>
              <path d="M158 30 L198 26 L238 36 L268 52 L282 72 L287 102 L277 132 L292 158 L296 188 L276 214 L261 244 L236 274 L206 293 L176 298 L151 283 L131 263 L117 233 L112 203 L117 173 L107 148 L112 118 L127 92 L138 66 L148 46 Z" fill="#E0F0E8" stroke="#B8D8C8" stroke-width="1.5"/>
              <circle cx="193" cy="82" r="5" fill="#18B25A" opacity=".85"/>
              <circle cx="163" cy="122" r="4" fill="#18B25A" opacity=".65"/>
              <circle cx="228" cy="142" r="6" fill="#18B25A"/>
              <circle cx="208" cy="182" r="3.5" fill="#18B25A" opacity=".6"/>
              <circle cx="178" cy="202" r="6" fill="#18B25A"/>
              <circle cx="158" cy="232" r="6" fill="#18B25A"/>
              <circle cx="183" cy="252" r="4" fill="#18B25A" opacity=".75"/>
              <circle cx="168" cy="278" r="5" fill="#18B25A" opacity=".85"/>
              <circle cx="143" cy="192" r="3" fill="#18B25A" opacity=".55"/>
              <circle cx="158" cy="232" r="14" stroke="#18B25A" stroke-width="1" opacity=".25"/>
              <circle cx="158" cy="232" r="22" stroke="#18B25A" stroke-width="1" opacity=".1"/>
              <circle cx="228" cy="142" r="12" stroke="#18B25A" stroke-width="1" opacity=".25"/>
              <rect x="238" y="128" width="52" height="18" rx="4" fill="rgba(24,178,90,.08)"/>
              <text x="264" y="141" font-family="DM Sans,sans-serif" font-size="10" fill="#18B25A" font-weight="600" text-anchor="middle">Nordeste</text>
              <rect x="80" y="222" width="58" height="18" rx="4" fill="rgba(24,178,90,.08)"/>
              <text x="109" y="235" font-family="DM Sans,sans-serif" font-size="10" fill="#18B25A" font-weight="600" text-anchor="middle">São Paulo</text>
              <rect x="22" y="22" width="108" height="56" rx="8" fill="white" stroke="#DDE9E3"/>
              <text x="34" y="45" font-family="Space Grotesk,sans-serif" font-size="21" fill="#0D1F17" font-weight="700">8+</text>
              <text x="34" y="59" font-family="DM Sans,sans-serif" font-size="10" fill="#8AADA0" font-weight="500">anos no automotivo</text>
              <text x="34" y="72" font-family="DM Sans,sans-serif" font-size="10" fill="#18B25A" font-weight="600">Todo o Brasil →</text>
              <rect x="0" y="314" width="400" height="34" fill="white"/>
              <line x1="0" y1="314" x2="400" y2="314" stroke="#DDE9E3" stroke-width="1"/>
              <circle cx="26" cy="331" r="4" fill="#18B25A"/>
              <text x="36" y="335" font-family="DM Sans,sans-serif" font-size="11" fill="#4A6B5A" font-weight="500">Concessionárias</text>
              <circle cx="148" cy="331" r="4" fill="#8AADA0"/>
              <text x="158" y="335" font-family="DM Sans,sans-serif" font-size="11" fill="#8AADA0" font-weight="500">Locadoras</text>
              <circle cx="238" cy="331" r="4" fill="#8AADA0"/>
              <text x="248" y="335" font-family="DM Sans,sans-serif" font-size="11" fill="#8AADA0" font-weight="500">Auto Centers</text>
            </svg>
          </div>
          <div class="pin pin--top">🏆 <strong>Presença nacional</strong><br/><small>Operações em todo o Brasil</small></div>
          <div class="pin pin--bot">🚀 <strong>Método comprovado</strong><br/><small>8 anos de resultados reais</small></div>
        </div>
      </div>
    </div>
  </section>
</template>

<script setup>
const pilares = [
  { icon: '🎯', title: 'Estratégia', desc: 'Campanhas que vendem' },
  { icon: '⚙️', title: 'Tecnologia', desc: 'CRM, IA e automações' },
  { icon: '📋', title: 'Processos', desc: 'Operação escalável' },
]
</script>

<style scoped>
.quem__layout { display: grid; grid-template-columns: 1fr 1fr; gap: 72px; align-items: center; margin-top: 48px; }
.quem__text p { font-size: 16px; color: var(--sub); line-height: 1.8; margin-bottom: 16px; }
.quem__text p strong { color: var(--ink); font-weight: 600; }
.pilares { display: grid; grid-template-columns: repeat(3,1fr); gap: 10px; margin-top: 26px; }
.pilar { background: var(--bg); border: 1px solid var(--bdr); border-radius: 10px; padding: 16px 12px; text-align: center; border-top: 2.5px solid var(--g); }
.pilar__icon { font-size: 18px; margin-bottom: 6px; }
.pilar h4 { font-family: 'Space Grotesk', sans-serif; font-size: 13px; font-weight: 700; color: var(--ink); }
.pilar p { font-size: 11px; color: var(--muted); margin-top: 3px; line-height: 1.4; margin-bottom: 0; }
.quem__visual { position: relative; }
.map-wrap { background: #fff; border: 1px solid var(--bdr); border-radius: 14px; overflow: hidden; box-shadow: var(--sh2); }
.map-wrap svg { width: 100%; display: block; }
.pin { position: absolute; background: #fff; border: 1px solid var(--bdr); border-radius: 10px; padding: 10px 14px; font-size: 12px; font-weight: 600; box-shadow: var(--sh2); line-height: 1.5; }
.pin strong { color: var(--ink); display: block; }
.pin small { font-size: 11px; color: var(--muted); font-weight: 500; }
.pin--top { top: -14px; right: -14px; border-left: 3px solid var(--g); }
.pin--bot { bottom: -14px; left: -14px; border-left: 3px solid var(--pk); }
@media (max-width: 900px) { .quem__layout { grid-template-columns: 1fr; } .quem__visual { display: none; } }
</style>
