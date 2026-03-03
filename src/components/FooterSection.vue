<template>
  <footer class="footer">
    <div class="container">
      <div class="footer__inner">
        <div class="footer__brand">
          <img src="../../public/assets/img/logo.webp" alt="CWA Digital" />
          <p>Especialistas em marketing digital, automação e crescimento para multimarcas e concessionárias. 8+ anos respirando o mercado automotivo.</p>
        </div>
        <div class="footer__col">
          <h4>Navegação</h4>
          <a href="#quem">Quem somos</a>
          <a href="#metodo">Método N.I.T.R.O</a>
          <a href="#pdi">PDI</a>
          <a href="#plano">Plano</a>
          <a href="#faq">FAQ</a>
        </div>
        <div class="footer__col">
          <h4>Contato</h4>
          <a href="#diagnostico">Agendar diagnóstico</a>
          <a href="#">Instagram</a>
          <a href="#">LinkedIn</a>
          <a href="#">WhatsApp</a>
        </div>
      </div>
      <div class="footer__bottom">
        <span>© 2025 CWA Digital. Todos os direitos reservados.</span>
        <span class="footer__powered">Powered by Garage HUB</span>
      </div>
    </div>
  </footer>
</template>

<style scoped>
.footer { background: #fff; border-top: 1px solid var(--bdr); padding: 56px 0 26px; }
.footer__inner { display: grid; grid-template-columns: 2fr 1fr 1fr; gap: 44px; }
.footer__brand img { height: 24px; object-fit: contain; display: block; }
.footer__brand p { font-size: 13px; color: var(--muted); margin-top: 12px; max-width: 250px; line-height: 1.7; }
.footer__col h4 { font-family: 'Space Grotesk', sans-serif; font-size: 11px; font-weight: 700; letter-spacing: 2px; text-transform: uppercase; color: var(--sub); margin-bottom: 13px; }
.footer__col a { display: block; font-size: 13px; color: var(--muted); text-decoration: none; margin-bottom: 8px; transition: color .2s; }
.footer__col a:hover { color: var(--g); }
.footer__bottom { margin-top: 32px; padding-top: 18px; border-top: 1px solid var(--bdr); display: flex; justify-content: space-between; align-items: center; font-size: 12px; color: var(--muted); }
.footer__powered { color: var(--g); font-weight: 600; }
@media (max-width: 900px) { .footer__inner { grid-template-columns: 1fr; gap: 26px; } .footer__bottom { flex-direction: column; gap: 6px; text-align: center; } }
</style>
