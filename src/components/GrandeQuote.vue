<template>
  <div class="gq-sec">
    <div class="container">
      <div class="gq">
        <img src="/logo-cwa.png" alt="CWA" class="gq__logo" />
        <p>"Empreender é, geralmente, uma jornada solitária. Raras são as vezes onde você pode realmente abrir seus planos e sonhos com alguém que fale sua língua. Nós somos muito mais que uma agência. <strong>Somos um parceiro para o crescimento da sua empresa. Batalharemos juntos nas trincheiras, superaremos desafios de forma criativa e brindaremos juntos cada conquista."</strong></p>
      </div>
    </div>
  </div>
</template>

<style scoped>
.gq-sec { background: linear-gradient(135deg, #E8175C 0%, #9C0A38 100%); padding: 88px 0; text-align: center; position: relative; overflow: hidden; }
.gq-sec::before { content: 'CWA'; position: absolute; top: 50%; left: 50%; transform: translate(-50%,-50%); font-family: 'Space Grotesk', sans-serif; font-size: 220px; font-weight: 700; color: rgba(255,255,255,.04); line-height: 1; pointer-events: none; user-select: none; }
.gq { max-width: 800px; margin: 0 auto; position: relative; z-index: 2; }
.gq__logo { height: 26px; object-fit: contain; filter: brightness(0) invert(1); opacity: .5; margin: 0 auto 26px; display: block; }
.gq p { font-size: clamp(17px, 2.2vw, 24px); font-weight: 400; line-height: 1.65; color: rgba(255,255,255,.9); font-style: italic; margin: 0; }
.gq p strong { color: #fff; font-style: normal; font-weight: 700; }
</style>
