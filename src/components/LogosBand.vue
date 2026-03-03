<template>
  <div class="logos-band">
    <div class="container logos-band__inner">
      <span class="logos-band__label">Canais gerenciados pela CWA</span>
      <div class="logos-band__list">
        <span v-for="canal in canais" :key="canal">{{ canal }}</span>
      </div>
    </div>
  </div>
</template>

<script setup>
const canais = ['Meta Ads', 'Google Ads', 'TikTok', 'WhatsApp', 'Instagram', 'Garage HUB CRM']
</script>

<style scoped>
.logos-band {
  border-top: 1px solid var(--bdr); border-bottom: 1px solid var(--bdr);
  padding: 15px 0; background: #fff;
}
.logos-band__inner { display: flex; align-items: center; justify-content: space-between; flex-wrap: wrap; gap: 14px; }
.logos-band__label { font-size: 10px; font-weight: 600; letter-spacing: 2px; text-transform: uppercase; color: var(--muted); }
.logos-band__list { display: flex; gap: 28px; flex-wrap: wrap; }
.logos-band__list span { font-family: 'Space Grotesk', sans-serif; font-size: 13px; font-weight: 600; color: var(--light); }
</style>
