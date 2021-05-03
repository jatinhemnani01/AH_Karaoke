<script context="module">
  export const hydrate = false;
  export const prerender = true;
  export const ssr = false;
</script>

<script>
  import { karaoke } from "$lib/karaoke";
  import ListComponent from "$lib/ListComponent.svelte";
</script>

<svelte:head>
  <title>Karaoke List</title>
</svelte:head>

{#each karaoke as item (item.id)}
  <ListComponent title={item.title} />
{/each}

<!-- <ListComponent title="Connexion Zayn Malik SOmethign" />
<ListComponent title="Connexion Zayn Malik SOmethign" />
<ListComponent title="Connexion Zayn Malik SOmethign" />
<ListComponent title="Connexion Zayn Malik SOmethign" />
<ListComponent title="Connexion Zayn Malik SOmethign" /> -->
