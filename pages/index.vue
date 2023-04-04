<template>
  <main class="grid grid-flow-row gap-8">
    <!-- Header -->
    <div class="flex items-center justify-between">
      <h1 class="text-[#0A0A0A] font-medium text-lg">Dashboard</h1>
      <div class="flex items-center space-x-4 text-sm">
        <button class="bg-[#212143] text-[#f5f5f5] rounded-md px-4 py-2 font-medium">
          <Icon name="material-symbols:add" size="1.3em" />
          Buddy Punching
        </button>
        <button class="text-[#212143] bg-[#FFFFFF] rounded-md px-4 py-2 font-medium">Manage POV</button>
      </div>
    </div>
    <!-- Header -->
    <!-- welcome greeting -->
    <div class="bg-white rounded-lg p-4 flex justify-between items-center">
      <div class="flex flex-col text-xs space-y-1">
        <p class="font-bold text-[#0A0A0A] text-sm">Good to see you Michael,</p>
        <p class="text-[10px] text-[#616161]">You came 15 minutes early today.</p>
      </div>
      <div class="flex items-center space-x-3">
        <div class="text-[10px] flex items-center space-x-2">
          <div class="bg-[#CEE5D3] text-[#0A7E22] flex items-center justify-center p-2 rounded"><Icon name="ph:arrow-line-left" size="2em" /></div>
          <div>
            <time class="text-[#404040] font-medium">7:14 AM</time>
            <p class="text-[#616161]">Punch in</p>
          </div>
        </div>
        <div class="text-[10px] flex items-center space-x-2">
          <div class="bg-[#FFD6DB] text-[#FD314D] flex items-center justify-center p-2 rounded"><Icon name="ph:arrow-line-right" size="2em" /></div>
          <div>
            <time class="text-[#404040] font-medium">5:00 PM</time>
            <p class="text-[#616161]">Punch Out</p>
          </div>
        </div>
      </div>
    </div>
    <!-- welcome greeting -->
  </main>
</template>
