<script>
  import { writable } from "svelte/store";
  // import GraphD3SVG from "./NetworkGraphD3SVG.svelte";
  // import GraphSvelteSVG from './NetworkGraphSvelteSVG.svelte';
  // import GraphCanvas from './NetworkGraphCanvas.svelte';
  // import GraphCanvasIdContext from './NetworkGraphCanvasIdContext.svelte';
  import lesMisData from './data/data-les-miserables.js';

  const rdfData = writable(0);
  const graph = writable(0);

  import RdfInterface from "./RdfInterface.svelte";
  import VisStore from "./RdfVisStore.svelte";

</script>

<style>
	h1 {
		color: purple;
	}
</style>

<h1>Svelte RDF Visualisation Lab</h1>
<RdfInterface></RdfInterface>
<!-- <VisStore {rdfData} {graph} /> -->
<!-- <GraphD3SVG {graph} /> -->
