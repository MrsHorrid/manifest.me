<script lang="ts">
    import "../app.css";
    import Menu from '$lib/icons/Menu.svelte';
    
    
  </script>
  
<nav class="p-8">
    <div class="flex justify-between items-center">
        <h1 class="font-bold text-2xl"><span class="text-[#8D86C9]">M</span>anifest.<span class="text-[#8D86C9]">me</span></h1>
        <Menu/>
    </div>

</nav>

<main>
    <slot/>
</main>


<style>
    :global(html)
    {
        background-color: #F7ECE1;
        font-family: 'Poppins', sans-serif;
    }
</style>