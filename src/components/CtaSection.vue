<template>
  <section id="diagnostico" class="section section--cta cta-sec">
    <div class="cta-sec__orb"></div>
    <div class="cta-sec__dots"></div>
    <div class="container">
      <div class="cta-sec__cnt">
        <img src="../../public/assets/img/logo.webp" alt="CWA" class="cta-sec__logo" />
        <div class="cta-sec__pill">⏱ Os resultados começam com a decisão de hoje</div>
        <h2>Esse é o passo que pode<br/>transformar a história<br/>do <em>seu negócio.</em></h2>
        <p>Não deixe o futuro da sua empresa para amanhã. Agende um diagnóstico gratuito de 30 minutos — nosso time vai mostrar exatamente onde sua operação pode crescer.</p>
        <a href="#" class="btn btn--green btn--xl">🚀 Vamos acelerar juntos agora →</a>
        <p class="cta-sec__fine">Sem compromisso · Sem enrolação · 100% gratuito · Resposta em até 24h</p>
      </div>
    </div>
  </section>
</template>

<style scoped>
.cta-sec { padding: 114px 0; position: relative; overflow: hidden; text-align: center; }
.cta-sec__orb { position: absolute; top: 50%; left: 50%; transform: translate(-50%,-50%); width: 640px; height: 640px; border-radius: 50%; background: radial-gradient(circle, rgba(24,178,90,.07), transparent 65%); }
.cta-sec__dots { position: absolute; inset: 0; background-image: radial-gradient(circle, rgba(24,178,90,.1) 1px, transparent 1px); background-size: 28px 28px; opacity: .25; }
.cta-sec__cnt { position: relative; z-index: 2; max-width: 680px; margin: 0 auto; }
.cta-sec__logo { height: 30px; object-fit: contain; filter: brightness(0) invert(1); opacity: .45; margin: 0 auto 28px; display: block; }
.cta-sec__pill { display: inline-block; background: rgba(24,178,90,.1); border: 1px solid rgba(24,178,90,.25); color: #34D680; font-size: 11px; font-weight: 600; letter-spacing: 2px; text-transform: uppercase; padding: 6px 15px; border-radius: 100px; margin-bottom: 24px; }
h2 { font-size: clamp(34px, 4.8vw, 58px); color: #fff; margin-bottom: 0; }
h2 em { color: #34D680; font-style: normal; }
p { font-size: 17px; color: rgba(255,255,255,.55); margin: 16px 0 36px; line-height: 1.8; }
.btn--xl { font-size: 15px; padding: 17px 42px; }
.cta-sec__fine { font-size: 12px; color: rgba(255,255,255,.28); margin: 14px 0 0; }
</style>
