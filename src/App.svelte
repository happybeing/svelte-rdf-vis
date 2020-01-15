<script>
  import NetworkGraphD3SVG from "./NetworkGraphD3SVG.svelte";
  // import GraphSvelteSVG from './NetworkGraphSvelteSVG.svelte';
  import NetworkGraphCanvas from './NetworkGraphCanvas.svelte';
  import RdfInterface from "./RdfInterface.svelte";
  import VisStore from "./RdfVisStore.svelte";

  import {graph} from "./stores.js";

</script>

<style>
	h1 {
		color: purple;
	}
</style>

<h1>Svelte RDF Visualisation Lab</h1>
<p>An app for prototyping RDF visualisation components 
built using Sveltejs and D3js. Code on <a href="https://github.com/theWebalyst/svelte-rdf-vis">github</a>.
</p>
<p>RdfInterface loads the RDF,  
<RdfInterface/>
VisStore maps the RDF to objects for visualisation,
<VisStore/>
NetworkGraphCanvas uses d3-force to display the graph.</p>
<NetworkGraphCanvas {graph} />
