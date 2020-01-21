<script>
  import NetworkGraphD3SVG from "./NetworkGraphD3SVG.svelte";
  // import GraphSvelteSVG from './NetworkGraphSvelteSVG.svelte';
  import NetworkGraphCanvas from './NetworkGraphCanvas.svelte';
  import RdfInterface from "./RdfInterface.svelte";
  import RdfVisStore from "./RdfVisStore.svelte";

  import {graph} from "./stores.js";

</script>

<style>
	h1 {
		color: purple;
	}
</style>

<h1>Svelte RDF Visualisation Lab</h1>
<p>This app is for prototyping RDF visualisation components build using Sveltejs and D3js. Code on <a href="https://github.com/theWebalyst/svelte-rdf-vis">github</a>.
</p>
<p>Loaded using RdfInterface. 
<RdfInterface/>
Mapped using RdfVisStore.
<RdfVisStore/>
Graph using NetworkGraphCanvas.</p>
<NetworkGraphCanvas {graph} />
