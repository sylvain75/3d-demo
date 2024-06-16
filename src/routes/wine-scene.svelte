<script lang="ts">
	import { T, useFrame } from '@threlte/core'
	import { OrbitControls, useGltf } from '@threlte/extras'
	import Bloom from './bloom.svelte'

	let y = 2
	let rotation = 0

	// Spooky floating ghost 👻
	function levitate() {
		const time = Date.now() / 1000
		const speed = 1
		const offset = 3
		y = Math.sin(time * speed) + offset
		requestAnimationFrame(levitate)
	}

	// Rotates model on `Y` axis
	useFrame((_, delta) => {
		rotation += delta * 0.4
	})

	// levitate()
</script>

<!-- Bloom postprocessing effect -->
<Bloom />

<!-- Orthographic camera -->
<T.OrthographicCamera position={[10, 10, 10]} zoom={40} makeDefault>
	<!-- Controls -->
	<OrbitControls enableDamping />
</T.OrthographicCamera>

<!-- Ambient light for ambience -->
<T.AmbientLight color="#0000ff" intensity={10} />

<!-- Main light -->
<T.PointLight intensity={2} position={[4, 2, 4]} color="#76aac8" />

<!-- Ghost -->
{#await useGltf('/assets/wine_bottle.glb') then wine}
	<T is={wine.scene} position={[0, y, 0]} scale={0.8} />
{/await}
