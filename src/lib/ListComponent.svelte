<script>
  export let title;
</script>

<div class="bg-blue-600 flex m-1 p-2 rounded-lg justify-between items-center">
  <div class="text-white">{title}</div>
  <a
    href="https://api.whatsapp.com/send?phone=919329023244&text={title}"
    class="text-white no-underline pr-4"
    ><i class="fa fa-whatsapp" style="font-size:48px;color:lightgreen" /></a
  >
</div>
