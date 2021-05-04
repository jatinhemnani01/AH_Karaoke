<script context="module">
  export const prerender = true;
</script>

<script>
  import { karaoke } from "$lib/karaoke";
  import ListComponent from "$lib/ListComponent.svelte";
  import ScrollToTop from "$lib/ScrollToTop.svelte";
  let search = "";
  let list = karaoke;

  function searchSong() {
    list = karaoke;
    let filteredArray = list.filter((item) =>
      item.title.toLowerCase().includes(search.toLowerCase())
    );
    list = filteredArray;
  }
</script>

<svelte:head>
  <title>Karaoke List</title>
  <meta
    name="description"
    content="Search Your Favourite Karaoke on AH Karaoke. Buy High Quality Karaoke With Just One Call or Message on AH Karaoke With Over 3000+ Karaokes."
  />
  <meta
    name="keywords"
    content="karaoke, ah karaoke, ahk, high quality karaoke, buy karaoke,search karaoke,search,bollywood, bollywood karaoke, karaoke hindi, hindi karaoke bollywood "
  />
  <meta name="author" content="Anil Hemnani" />
</svelte:head>

<form
  on:submit|preventDefault={searchSong}
  class="flex justify-center p-8 bg-pink-700"
>
  <input
    placeholder="Search Karaoke Here"
    type="text"
    bind:value={search}
    class="lg:w-3/6 md:w-3/6 w-11/12 h-8 p-2 rounded-lg focus:outline focus:ring focus:border-green-600"
  />
  <input
    type="submit"
    value="Search"
    class="w-24 bg-green-600 text-white rounded-lg"
  />
</form>

{#if list === null || list.length === 0}
  <h2 class="text-2xl text-center p-5">
    Song Not Available. If you want we can make it.
  </h2>
  <strong
    ><a class="flex justify-center text-center text-xl" href="tel:9329023244"
      >Call Here</a
    ></strong
  >
{/if}

{#each list as item (item.id)}
  <ListComponent title={item.title} />
{/each}

<ScrollToTop />
