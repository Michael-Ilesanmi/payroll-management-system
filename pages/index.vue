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
    <!-- Leave Overview / Summary -->
    <div class="bg-white grid grid-cols-4 grid-rows-1 gap-8 rounded-lg py-4 px-8">
      <div class="space-y-2 border-r border-[#E0E0E0]">
        <h4 class="text-[#404040] font-medium">
          Total leave allowance
        </h4>
        <p class="text-[#146ADC] text-2xl font-medium">
          24
        </p>
        <div class="flex space-x-4 text-xs text-[#9E9E9E]">
          <p>Paid <span class="text-[#146ADC]">11</span></p>
          <p>Paid <span class="text-[#D32940]">13</span></p>
        </div>
      </div>
      <div class="space-y-2 border-r border-[#E0E0E0]">
        <h4 class="text-[#404040] font-medium">
          Total leave taken
        </h4>
        <p class="text-[#146ADC] text-2xl font-medium">
          20
        </p>
        <div class="flex space-x-4 text-xs text-[#9E9E9E]">
          <p>Paid <span class="text-[#146ADC]">11</span></p>
          <p>Paid <span class="text-[#D32940]">9</span></p>
        </div>
      </div>
      <div class="space-y-2 border-r border-[#E0E0E0]">
        <h4 class="text-[#404040] font-medium">
          Total leave available
        </h4>
        <p class="text-[#146ADC] text-2xl font-medium">
          87
        </p>
        <div class="flex space-x-4 text-xs text-[#9E9E9E]">
          <p>Paid <span class="text-[#146ADC]">50</span></p>
          <p>Paid <span class="text-[#D32940]">37</span></p>
        </div>
      </div>
      <div class="space-y-2">
        <h4 class="text-[#404040] font-medium">
          Leave requests pending
        </h4>
        <p class="text-[#146ADC] text-2xl font-medium">
          122
        </p>
        <div class="flex space-x-4 text-xs text-[#9E9E9E]">
          <p>Paid <span class="text-[#146ADC]">60</span></p>
          <p>Paid <span class="text-[#D32940]">62</span></p>
        </div>
      </div>
    </div>
    <!-- Leave Overview / Summary -->
    <!-- Time Log -->
    <div class="bg-white rounded-lg py-4 px-8">
      <h2 class="text-[#0A0A0A] font-bold mb-6">Time Log</h2>
      <div class="grid grid-cols-2">
        <div class="border-r pr-6">
          <h3 class="mb-4 font-medium text-[#404040]">Today</h3>
          <div class="grid grid-flow-col justify-between">
            <div class="bg-[#F5F5F5] rounded-lg p-4 space-y-2">
              <p class="text-[#404040] font-medium text-sm">08:00</p>
              <p class="text-xs text-[#9E9E9E]">Scheduled</p>
            </div>
            <div class="bg-[#F5F5F5] rounded-lg p-4 space-y-2">
              <p class="text-[#404040] font-medium text-sm">12:00</p>
              <p class="text-xs text-[#9E9E9E]">Balance</p>
            </div>
            <div class="bg-[#F5F5F5] rounded-lg p-4 space-y-2">
              <p class="text-[#404040] font-medium text-sm">05:00</p>
              <p class="text-xs text-[#9E9E9E]">Worked</p>
            </div>
          </div>
        </div>
        <div class="pl-6">
          <h3 class="mb-4 font-medium text-[#404040]">This month</h3>
          <div class="grid grid-cols-2 gap-6 justify-between">
            <div class="space-y-3">
              <div class="flex items-center justify-between font-medium text-xs">
                <p class="text-[#9E9E9E]">Total</p>
                <p class="text-[#404040]">216 hour</p>
              </div>
              <div class="rounded-full w-full h-3 bg-[#F5F5F5] overflow-clip">
                <div class="h-full w-3/12 bg-[#146ADC]"></div>
              </div>
            </div>
            <div class="space-y-3">
              <div class="flex items-center justify-between font-medium text-xs">
                <p class="text-[#9E9E9E]">Worked time</p>
                <p class="text-[#404040]">189 hour</p>
              </div>
              <div class="rounded-full w-full h-3 bg-[#F5F5F5] overflow-clip">
                <div class="h-full w-4/12 bg-[#146ADC]"></div>
              </div>
            </div>
            <div class="space-y-3">
              <div class="flex items-center justify-between font-medium text-xs">
                <p class="text-[#9E9E9E]">Shortage time</p>
                <p class="text-[#404040]">23 hour</p>
              </div>
              <div class="rounded-full w-full h-3 bg-[#F5F5F5] overflow-clip">
                <div class="h-full w-5/12 bg-[#146ADC]"></div>
              </div>
            </div>
            <div class="space-y-3">
              <div class="flex items-center justify-between font-medium text-xs">
                <p class="text-[#9E9E9E]">Over time</p>
                <p class="text-[#404040]">56 hour</p>
              </div>
              <div class="rounded-full w-full h-3 bg-[#F5F5F5] overflow-clip">
                <div class="h-full w-7/12 bg-[#146ADC]"></div>
              </div>
            </div>
          </div>
        </div>
      </div>
    </div>
    <!-- Time Log -->
    <!-- Announcements -->
    <div class="bg-white rounded-lg py-4 px-8">
      <h2 class="text-[#0A0A0A] font-bold mb-6">Announcements</h2>
      <table class="w-full">
        <thead>
          <td>Title</td>
          <td>Start Date</td>
          <td>End Date</td>
          <td>Description</td>
        </thead>
        <tbody>
          <tr>
            <td>Scrum Master</td>
            <td>Dec 4, 2019 21:42</td>
            <td>Dec 4, 2019 21:42</td>
            <td>Lorem ipsum dolor sit amet.</td>
          </tr>
          <tr>
            <td>Scrum Master</td>
            <td>Dec 4, 2019 21:42</td>
            <td>Dec 4, 2019 21:42</td>
            <td>Lorem ipsum dolor sit amet.</td>
          </tr>
          <tr>
            <td>Scrum Master</td>
            <td>Dec 4, 2019 21:42</td>
            <td>Dec 4, 2019 21:42</td>
            <td>Lorem ipsum dolor sit amet.</td>
          </tr>
          <tr>
            <td>Scrum Master</td>
            <td>Dec 4, 2019 21:42</td>
            <td>Dec 4, 2019 21:42</td>
            <td>Lorem ipsum dolor sit amet.</td>
          </tr>
        </tbody>
      </table>      
    </div>
    <!-- Announcements -->
  </main>
</template>

<style lang="scss" scoped>
table {
  thead {
    @apply bg-[#F5F5F5] text-xs text-[#0A0A0A];
    td{
      @apply py-2 border-r border-[#E0E0E0] px-4 last:border-none;
    }
  }
  tbody{
    @apply text-xs text-[#0A0A0A];
    tr {
      @apply hover:bg-[#F4F4F4] cursor-pointer transition-colors ease-in-out;
      td{
        @apply py-2 px-4;
      }
    }
  }
}
</style>