<!--
Auto-generated by: https://github.com/threlte/threlte/tree/main/packages/gltf
Command: npx @threlte/gltf@0.0.5 wine_bottle.glb
Author: sotocodes (https://sketchfab.com/sotocodes)
License: CC-BY-4.0 (http://creativecommons.org/licenses/by/4.0/)
Source: https://sketchfab.com/3d-models/wine-bottle-651e6b77329043ecb89cf5e75f5fe209
Title: Wine Bottle
-->

<script>
  import { Group } from 'three'
  import { T, Three } from '@threlte/core'
  import { useGltf } from '@threlte/extras'

  export const ref = new Group()

  const { gltf } = useGltf('/wine_bottle.glb')
</script>

{#if $gltf}
  <Three type={ref} {...$$restProps}>
    <T.Group rotation={[-Math.PI / 2, 0, 0]}>
      <T.Mesh
        geometry={$gltf.nodes['Material_003-material'].geometry}
        material={$gltf.materials.Material_003}
        position={[0, 0, -2.38]}
        scale={0.87}
      />
      <T.Mesh
        geometry={$gltf.nodes['Material_002-material'].geometry}
        material={$gltf.materials.Material_002}
        position={[0, 0, -2.41]}
        scale={0.87}
      />
      <T.Mesh
        geometry={$gltf.nodes['Material_002-material_1'].geometry}
        material={$gltf.materials.Material_002}
        position={[0, 0, -2.38]}
        scale={0.87}
      />
      <T.LineSegments
        geometry={$gltf.nodes.Object_9.geometry}
        material={$gltf.materials.Cylinder_000}
        position={[0, 0, -2.38]}
        scale={0.87}
      />
      <T.Mesh
        geometry={$gltf.nodes['Material_001-material'].geometry}
        material={$gltf.materials.Material_001}
        position={[0, 0, -2.38]}
        scale={0.87}
      />
      <T.Mesh
        geometry={$gltf.nodes['Material_005-material'].geometry}
        material={$gltf.materials.Material_005}
        position={[0, 0, -2.38]}
        scale={0.87}
      />
    </T.Group>

    <slot {ref} />
  </Three>
{/if}
