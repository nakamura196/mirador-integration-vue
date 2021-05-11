<template>
  <div id="app">
    <div id="demo"></div>
  </div>
</template>

<script>
import Mirador from 'mirador/dist/es/src/index';
import { miradorImageToolsPlugin } from 'mirador-image-tools';

export default {
  name: 'App',
  mounted(){
    const config = {
      id: 'demo',
      windows: [{
        imageToolsEnabled: true,
        imageToolsOpen: true,
        manifestId: 'https://purl.stanford.edu/sn904cj3429/iiif/manifest',
      }],
    };

    Mirador.viewer(config, [
      ...miradorImageToolsPlugin,
    ]);
  }
}
</script>
