<script context="module">
  export const prerender = true;
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
