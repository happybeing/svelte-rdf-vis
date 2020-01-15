<script>
  import GraphD3SVG from "./NetworkGraphD3SVG.svelte";
  // import GraphSvelteSVG from './NetworkGraphSvelteSVG.svelte';
  import GraphCanvas from './NetworkGraphCanvas.svelte';
  // import GraphCanvasIdContext from './NetworkGraphCanvasIdContext.svelte';
  // import lesMisData from './data/data-les-miserables.js';
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
<p>Loaded using RdfInterface</p>
<RdfInterface/>
<p>Mapped using VisStore</p>
<VisStore/>
<p>Graph using GraphCanvas</p>
<GraphCanvas {graph} />
