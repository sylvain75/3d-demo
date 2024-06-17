<script>
	import "../app.css";
</script>

<div class="scene">
	<slot />
</div>

<svelte:head>
	<title>Threlte</title>
</svelte:head>

<style>
  .scene {
    position: absolute;
    inset: 0;
    background: radial-gradient(hsl(182, 100%, 94%), hsl(182, 100%, 74%));
  }
</style>
