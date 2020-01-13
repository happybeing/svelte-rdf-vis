<!-- Svelte wrapper for an RDF data sources (files, LDP, Solid etc.)

A basis for a generic Svelte component that interfaces to different 
RDF sources using different libraries.

Initially using rdflib to obtain RDF as a blob, later the interface to the
application components can be revised (e.g. to support streaming or supplying
a triple store etc.)

-->

<script>
import { onMount } from 'svelte';

const readTtl = require('@graphy/content.ttl.read');

console.log('Graphy...');

$: triples = [];

onMount(() => {
  readTtl(`
      @prefix foaf: <http://xmlns.com/foaf/0.1/> .

      <#spiderman> a foaf:Person ;
          foaf:name "Spiderman" .
  `, {
      data(y_quad) {
          console.log(JSON.stringify(y_quad));
          triples.push(y_quad);
          triples = triples;
      },

      eof(h_prefixes) {
          console.log('done!');
      },
  })
});

</script>

<div><h2>Graphy</h2>
<ul>
	{#each triples as triple, i}
		<li>wut {triple}</li>
	{/each}
</ul>
</div>