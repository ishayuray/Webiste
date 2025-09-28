<script lang="ts">
  import "./app.css"
  import {Menu, X} from '@lucide/svelte';
  let isMenuOpen = false
</script>
<!-- Why are navbars such a pain?? -->
<nav class="p-3 pl-10 pr-10 flex items-center justify-between">
  <h1 class="text-xl"> 
    <a href="/"> Ishayu Ray </a>
  </h1>
  <div class="flex gap-3 max-md:hidden">
    <a href="#about"> About Me </a>
    <a href="#contact"> Contact Me </a>
  </div>
  <Menu class={(!isMenuOpen)? "min-md:hidden" : "hidden"} onclick={() => isMenuOpen = !isMenuOpen}/>
  <X class={(isMenuOpen)? "min-md:hidden" : "hidden"} onclick={() => isMenuOpen = !isMenuOpen}/>
</nav>
<div class={(isMenuOpen)?"flex flex-col items-center justify-center min-md:hidden" : "hidden"}>
  <a href="#about"> About Me </a>
  <a href="#contact"> Contact Me </a>  
</div>
<article class="flex flex-col justify-center items-center text-center pl-10 pr-10 p-3 h-[90vh]" id="about">
  <h1 class="text-4xl text-yellow-300 p-3 font-mono"> Ishayu Ray</h1>
  <p> Hi! I'm Ishayu Ray, a high school student. </p>
  <p> This is my website.</p>
  <a href="#contact" class="p-2 m-3 bg-yellow-300 text-black font-semibold rounded-2xl pl-10 pr-10 hover:bg-yellow-100"> Contact Me </a>
</article>
<article id ="contact" class="flex flex-col justify-center items-center text-center pl-10 pr-10 p-3">
  <h1 class="text-2xl"> Contact Me </h1>
  <p> You can contact me at <a href="mailto:theishayuray@gmail.com" class="text-blue-400 underline">theishayuray@gmail.com</a> </p>
</article>