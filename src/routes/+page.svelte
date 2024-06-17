
<script lang="ts">
	import { Canvas } from '@threlte/core'
	import WineScene from './wine-scene.svelte'
	// import Scene from './scene.svelte'
</script>
<!--linear-gradient(135deg, #4cb3e7 0, #3775b9 100%);-->
<div class="absolute left-[55%] top-[30%]">
	<img src="/assets/up-go-logo.png" alt="" class="w-[200px] h-[200px] relative">
	<p class="text-[80px] font-extrabold text-white bg-[#3775b9] rounded-full p-0 absolute right-[-65%] top-[-5%] -rotate-12 italic p-2">ON</p>
</div>
<Canvas>
	<WineScene />
</Canvas>
