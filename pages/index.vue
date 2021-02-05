<template>
  <div class=" h-screen  flex flex-col items-center justify-center bg-gradient-to-b from-pink-300 via-red-200 to-yellow-100">

    <div id="music-container" class="  bg-gray-100 rounded-lg shadow-2xl flex px-4 py-2 mt-16 z-10 w-64 relative">
      <transition 
            enter-active-class="transition-opacity ease-linear duration-500"
            leave-active-class="transition-opacity ease-linear duration-300"
            enter-class="opacity-0"
            enter-to-class="opacity-100"
            leave-class="opacity-100"
            leave-to-class="opacity-0"
    >
      <div v-show="isPlaying" class="music-info bg-gray-100 bg-opacity-50 rounded-t-xl absolute top-0 left-6 w-10/12 pt-1 pr-1 pl-16 transform -translate-y-full "
       
      >
        <h4 id="title" class=" text-xs">ukulele</h4>
        <div class="progress-container bg-gray-50 rounded-lg cursor-pointer my-2 h-1 w-100" id="progress-container">
          <div class="progress bg-pink-400 h-full rounded-lg w-3/6"></div>
        </div>
      </div>
      </transition>

      <audio src="/music/ukulele.mp3" id="audio"></audio>
      <div class="image-container relative w-16 flex justify-center">
        <img class="cover-image rounded-full object-cover h-16 w-16 absolute bottom-0 left-0 z-40 " :class="{'animate-spin': isPlaying}"  src="/images/ukulele.jpg" alt="music-cover" id="cover">
        <div class="absolute bg-gray-100 h-4 w-4 rounded-full top-0 z-40"></div>
      </div>
      <div class="navigation mx-auto flex items-center justify-center z-30">
        <button id="prev">
          <svg class="w-6 h-6 text-red-300" fill="currentColor" stroke="currentColor" viewBox="0 0 24 24" xmlns="http://www.w3.org/2000/svg"><path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M12.066 11.2a1 1 0 000 1.6l5.334 4A1 1 0 0019 16V8a1 1 0 00-1.6-.8l-5.333 4zM4.066 11.2a1 1 0 000 1.6l5.334 4A1 1 0 0011 16V8a1 1 0 00-1.6-.8l-5.334 4z"></path></svg>
        </button>
        <button id="play" @click="isPlaying = !isPlaying">
          <svg class="w-10 h-10 mx-1 text-red-300" fill="currentColor" viewBox="0 0 20 20" xmlns="http://www.w3.org/2000/svg"><path fill-rule="evenodd" d="M10 18a8 8 0 100-16 8 8 0 000 16zM9.555 7.168A1 1 0 008 8v4a1 1 0 001.555.832l3-2a1 1 0 000-1.664l-3-2z" clip-rule="evenodd"></path></svg>
        </button>
        <button id="next"> 
          <svg class="w-6 h-6 text-red-300" fill="currentColor" stroke="currentColor" viewBox="0 0 24 24" xmlns="http://www.w3.org/2000/svg"><path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M11.933 12.8a1 1 0 000-1.6L6.6 7.2A1 1 0 005 8v8a1 1 0 001.6.8l5.333-4zM19.933 12.8a1 1 0 000-1.6l-5.333-4A1 1 0 0013 8v8a1 1 0 001.6.8l5.333-4z"></path></svg>
        </button>
        
      </div>
    </div>
  </div>
</template>

<script>
export default {
  data: () => ({
      isPlaying: false,
    })
}
</script>

<style>

</style>
