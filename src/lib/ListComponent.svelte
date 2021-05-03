<script>
  export let title;
</script>

<svelte:head>
  <link
    rel="stylesheet"
    href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/4.7.0/css/font-awesome.min.css"
  />
</svelte:head>

<div class="bg-blue-600 flex m-1 p-2 rounded-lg justify-between items-center">
  <div class="text-white">{title}</div>
  <a
    target="_blank"
    href="https://api.whatsapp.com/send?phone=919329023244&text={title}"
    class="text-white no-underline pr-4"
    ><i class="fa fa-whatsapp" style="font-size:48px;color:lightgreen" /></a
  >
</div>
