<template>
  <div class="flex min-h-screen bg-[#1B0E2F] text-white font-sans">
    <!-- Sidebar -->
    <aside class="w-64 bg-gradient-to-b from-[#2A1C3E] to-[#1B0E2F] p-6 flex flex-col shadow-2xl">
      <h1 class="text-3xl font-extrabold text-[#FFCB05] mb-8 tracking-widest">MelaHost</h1>
      <nav class="flex-1 space-y-3">
        <a href="#" class="flex items-center gap-3 px-3 py-2 rounded-lg hover:bg-[#FFCB05]/10 transition group">
          <span class="text-[#FFCB05] group-hover:translate-x-1 transition">🏠</span>
          <span class="group-hover:text-[#FFCB05] transition">Dashboard</span>
        </a>
        <a href="#" class="flex items-center gap-3 px-3 py-2 rounded-lg hover:bg-[#FFCB05]/10 transition group">
          <span class="text-[#FFCB05] group-hover:translate-x-1 transition">📁</span>
          <span class="group-hover:text-[#FFCB05] transition">File Manager</span>
        </a>
        <a href="#" class="flex items-center gap-3 px-3 py-2 rounded-lg hover:bg-[#FFCB05]/10 transition group">
          <span class="text-[#FFCB05] group-hover:translate-x-1 transition">👥</span>
          <span class="group-hover:text-[#FFCB05] transition">User Roles</span>
        </a>
        <a href="#" class="flex items-center gap-3 px-3 py-2 rounded-lg hover:bg-[#FFCB05]/10 transition group">
          <span class="text-[#FFCB05] group-hover:translate-x-1 transition">⚙️</span>
          <span class="group-hover:text-[#FFCB05] transition">Settings</span>
        </a>
      </nav>
      <button class="mt-auto flex items-center gap-2 px-4 py-2 rounded-md bg-[#FFCB05] hover:bg-yellow-400 text-black font-semibold transition shadow-xl">
        🚪 Logout
      </button>
    </aside>

    <!-- Main Content -->
    <main class="flex-1 p-8 lg:p-12 space-y-10 animate-fade-in">
      <h2 class="text-4xl font-bold text-[#FFCB05] mb-4">Game Panel</h2>

      <div class="grid 2xl:grid-cols-3 md:grid-cols-2 gap-8">
        <!-- Server Control Card -->
        <div class="bg-[#2A1C3E] p-6 rounded-2xl shadow-xl hover:shadow-2xl transition space-y-5 animate-slide-up">
          <h3 class="text-xl font-semibold flex items-center gap-2"><span>🎮</span> Server Control</h3>
          <button class="w-full flex items-center justify-center gap-2 bg-green-500 hover:bg-green-600 text-black font-bold py-2 rounded-md transition shadow-md">
            ▶️ Start
          </button>
          <button class="w-full flex items-center justify-center gap-2 bg-yellow-400 hover:bg-yellow-500 text-black font-bold py-2 rounded-md transition shadow-md">
            🔄 Restart
          </button>
          <button class="w-full flex items-center justify-center gap-2 bg-red-600 hover:bg-red-700 text-white font-bold py-2 rounded-md transition shadow-md">
            ⏹ Stop
          </button>
        </div>

        <!-- Console Card -->
        <div class="bg-[#2A1C3E] p-6 rounded-2xl shadow-xl hover:shadow-2xl transition space-y-4 animate-slide-up">
          <h3 class="text-xl font-semibold flex items-center gap-2"><span>📜</span> Console</h3>
          <div class="bg-black/90 p-4 h-60 overflow-y-scroll text-green-400 rounded-md font-mono text-sm ring-1 ring-gray-700">
            <p>[13:45:10] Server started on port 25565...</p>
            <p>[13:45:12] Player Obskron joined the game.</p>
            <p>[13:46:05] Saved the game.</p>
          </div>
          <div class="flex gap-2">
            <input type="text" placeholder="Type command..." class="flex-1 p-2 rounded-md text-black" />
            <button class="px-4 py-2 rounded-md bg-[#FFCB05] hover:bg-yellow-400 text-black font-semibold shadow-md">Send</button>
          </div>
        </div>

        <!-- Server Stats Card -->
        <div class="bg-[#2A1C3E] p-6 rounded-2xl shadow-xl hover:shadow-2xl transition space-y-6 animate-slide-up">
          <h3 class="text-xl font-semibold flex items-center gap-2"><span>📊</span> Server Stats</h3>
          <!-- RAM -->
          <div>
            <div class="flex justify-between text-sm mb-1">
              <span>RAM Usage</span>
              <span class="text-[#FFCB05]">1.2 GB / 4 GB</span>
            </div>
            <div class="h-2 bg-gray-600 rounded-full">
              <div class="h-full bg-[#FFCB05] rounded-full w-[30%]"></div>
            </div>
          </div>
          <!-- Disk -->
          <div>
            <div class="flex justify-between text-sm mb-1">
              <span>Disk Usage</span>
              <span class="text-[#FFCB05]">8.5 GB / 30 GB</span>
            </div>
            <div class="h-2 bg-gray-600 rounded-full">
              <div class="h-full bg-[#FFCB05] rounded-full w-[28%]"></div>
            </div>
          </div>
          <!-- Status -->
          <div class="flex items-center gap-2 text-sm">
            <span>Status</span>
            <span class="px-2 py-1 bg-green-700 text-green-100 rounded-full">Online</span>
          </div>
        </div>
      </div>
    </main>
  </div>
</template>

<script>
export default {
  name: "GamePanel"
};
</script>

<style scoped>
@keyframes fade-in {
  from { opacity: 0; }
  to { opacity: 1; }
}
@keyframes slide-up {
  from { opacity: 0; transform: translateY(40px); }
  to { opacity: 1; transform: translateY(0); }
}
.animate-fade-in { animation: fade-in 0.8s ease-out; }
.animate-slide-up { animation: slide-up 0.8s ease-out; }
</style>