<template>
  <!-- Full-width starfield background -->
  <div
    class="relative min-h-screen bg-gradient-to-b from-[#12091F] via-[#1B0E2F] to-black overflow-x-hidden text-white font-sans"
  >
    <!-- Grain overlay for subtle texture -->
    <div
      class="pointer-events-none absolute inset-0 bg-[url('https://grainy-gradients.vercel.app/noise.svg')] opacity-30 mix-blend-soft-light"
    ></div>

    <!-- ===== Navbar ==================================================== -->
     <header
      class="fixed top-0 inset-x-0 z-50 backdrop-blur-md bg-black/40 shadow-lg"
    >
      <div
        class="max-w-7xl mx-auto w-full flex items-center py-4 px-6 md:px-10"
      >
        <h1
          class="text-3xl font-extrabold text-white tracking-widest select-none items-center flex gap-2"
            > <!-- Logo -->
            <logoSvg :size="48"/>
          MelaHost
        </h1>

        <!-- Center navigation -->
        <nav class="hidden md:flex flex-1 justify-center gap-10 text-sm">
          <a href="#features" class="hover:text-[#FFCB05] transition"
            >Features</a
          >
          <a href="#plans" class="hover:text-[#FFCB05] transition">Plans</a>
          <a href="#contact" class="hover:text-[#FFCB05] transition"
            >Contact</a
          >
        </nav>

        <!-- Auth buttons -->
        <div class="flex items-center gap-4 text-sm">
          <a href="#login" class="hover:text-[#FFCB05] transition">Login</a>
          <a
            href="#signup"
            class="px-4 py-2 rounded-lg bg-[#FFCB05] text-black font-semibold hover:bg-yellow-400 transition shadow-xl"
          >
            Sign&nbsp;Up
          </a>
        </div>
      </div>
    </header>

    <!-- ===== Hero ====================================================== -->
    <section
      id="hero"
      class="relative flex flex-col justify-center items-center text-center pt-40 pb-32 px-6 md:px-10 overflow-hidden"
    >
      <!-- Blurry accent orb -->
      <div
        class="absolute -top-32 right-1/2 translate-x-1/2 w-[1000px] h-[1000px] bg-[#FFCB05]/20 rounded-full blur-3xl"
      ></div>

      <h2 class="text-5xl md:text-6xl font-extrabold leading-tight mb-6">
        <span
          class="bg-gradient-to-r from-[#FFCB05] via-yellow-300 to-white bg-clip-text text-transparent"
          >Next-Gen</span
        >
        Game&nbsp;Servers
      </h2>

      <p class="max-w-4xl text-gray-300 mb-10 text-lg md:text-xl">
        Ultra-low latency hosting crafted in Malta for Minecraft, Rust &amp;
        more. Launch your world in seconds and conquer the leaderboard.
      </p>

      <div class="flex flex-wrap justify-center gap-6">
        <a
          href="#plans"
          class="px-8 py-3 bg-[#FFCB05] hover:bg-yellow-400 text-black font-semibold rounded-lg shadow-lg transition"
          >View Plans</a
        >
        <a
          href="#features"
          class="px-8 py-3 border border-[#FFCB05] hover:bg-[#FFCB05]/10 rounded-lg transition"
          >Learn More</a
        >
      </div>
    </section>

    <!-- ===== Features ================================================== -->
    <section id="features" class="py-24 px-6 md:px-10 max-w-7xl mx-auto w-full">
      <div class="grid gap-10 md:grid-cols-3">
        <div class="feature-card animate-fade-in">
          <div class="text-4xl mb-4 select-none">⚡</div>
          <h3 class="feature-title">Instant Deployment</h3>
          <p class="feature-text">
            Spin up your server in under 30&nbsp;seconds with our automated
            wizard.
          </p>
        </div>

        <div class="feature-card animate-fade-in delay-100">
          <div class="text-4xl mb-4 select-none">🛡️</div>
          <h3 class="feature-title">DDoS&nbsp;Protection</h3>
          <p class="feature-text">
            Enterprise-grade shielding keeps griefers &amp; attacks at bay 24/7.
          </p>
        </div>

        <div class="feature-card animate-fade-in delay-200">
          <div class="text-4xl mb-4 select-none">🚀</div>
          <h3 class="feature-title">Blazing Performance</h3>
          <p class="feature-text">
            NVMe SSDs &amp; Ryzen CPUs push tick rates to the max for silky
            gameplay.
          </p>
        </div>
      </div>
    </section>

    <!-- ===== Plans ===================================================== -->
    <section
      id="plans"
      class="py-24 bg-gradient-to-b from-[#1E1233] to-[#12091F] px-6 md:px-10 max-w-7xl mx-auto w-full"
    >
      <h2
        class="text-4xl font-bold text-center mb-14 animate-fade-in select-none"
      >
        Choose Your Power Level
      </h2>

      <div class="grid gap-8 md:grid-cols-3">
        <!-- Starter -->
        <div class="plan-card animate-slide-up">
          <h3 class="plan-title">Starter</h3>
          <p class="plan-price">
            €5<span class="plan-duration">/mo</span>
          </p>
          <ul class="plan-list">
            <li>1 GB RAM</li>
            <li>10 GB NVMe</li>
            <li>Minecraft only</li>
          </ul>
          <a href="#" class="plan-btn">Get&nbsp;Started</a>
        </div>

        <!-- Pro Gamer -->
        <div class="plan-card featured-plan animate-slide-up delay-100">
          <span class="badge-popular">Popular</span>
          <h3 class="plan-title">Pro&nbsp;Gamer</h3>
          <p class="plan-price">
            €15<span class="plan-duration">/mo</span>
          </p>
          <ul class="plan-list text-black">
            <li>4 GB RAM</li>
            <li>30 GB NVMe</li>
            <li>Any game</li>
          </ul>
          <a href="#" class="plan-btn dark-btn">Start&nbsp;Hosting</a>
        </div>

        <!-- Clan Tier -->
        <div class="plan-card animate-slide-up delay-200">
          <h3 class="plan-title">Clan&nbsp;Tier</h3>
          <p class="plan-price">
            €30<span class="plan-duration">/mo</span>
          </p>
          <ul class="plan-list">
            <li>8 GB RAM</li>
            <li>80 GB NVMe</li>
            <li>Voice server included</li>
          </ul>
          <a href="#" class="plan-btn">Rule&nbsp;the&nbsp;Realm</a>
        </div>
      </div>
    </section>

    <!-- ===== Newsletter =============================================== -->
    <section class="py-24 px-6 md:px-10 text-center animate-fade-in">
      <h2 class="text-3xl font-bold mb-4">Stay in the Loop</h2>
      <p class="mb-8 text-gray-300">
        Get discounts, patch notes &amp; server tips straight to your inbox.
      </p>

      <form
        @submit.prevent="subscribe"
        class="max-w-xl mx-auto flex flex-col sm:flex-row gap-4"
      >
        <input
          v-model="email"
          type="email"
          placeholder="Your email"
          required
          class="flex-1 px-4 py-3 rounded-lg text-black"
        />
        <button
          type="submit"
          class="px-6 py-3 rounded-lg bg-[#FFCB05] hover:bg-yellow-400 text-black font-semibold shadow-lg transition"
        >
          Subscribe
        </button>
      </form>
    </section>

    <!-- ===== Footer ==================================================== -->
    <footer
      id="contact"
      class="border-t border-white/10 backdrop-blur-md bg-black/30 py-10 text-center text-sm"
    >
      <p class="mb-2">
        Have questions?
        <a href="mailto:contact@melahost.mt" class="text-[#FFCB05] underline"
          >Email us</a
        >
      </p>
      <p class="text-gray-500">© 2025 MelaHost — Made in Malta 🇲🇹</p>
    </footer>
  </div>
</template>

<script>
import Logo from './Logo.vue';
export default {
  name: "LandingPageFullWidth",
  data() {
    
    return { email: "" };
  },
  components: {
    LogoSvg: Logo,
  },
  methods: {
    subscribe() {
      alert(`Thanks for subscribing with: ${this.email}`);
      this.email = "";
    },
  },
};
</script>

<style scoped>
/* ---------- Animations ---------- */
@keyframes fade-in {
  from {
    opacity: 0;
  }
  to {
    opacity: 1;
  }
}
@keyframes slide-up {
  from {
    opacity: 0;
    transform: translateY(40px);
  }
  to {
    opacity: 1;
    transform: translateY(0);
  }
}
.animate-fade-in {
  animation: fade-in 0.8s ease-out both;
}
.animate-slide-up {
  animation: slide-up 0.8s ease-out both;
}
.delay-100 {
  animation-delay: 0.1s;
}
.delay-200 {
  animation-delay: 0.2s;
}

</style>
