<script lang="ts">
    import { fade, fly, blur } from 'svelte/transition';
    let manifestations:any = []
    let typed = ''
    let released = false
    let isEntered = false
    import src from "$lib/icons/ph_sparkle.png"
    import sparkly from "$lib/icons/filled.png"
    

    function addToList()
    {
        manifestations = [...manifestations , typed]
        typed = ''
        isEntered = true
    }

    function releaseManifestation()
    {
        released = true
        manifestations = []
        isEntered = false
        
    }
</script>

<div class="mt-5">
    <label>
    
        <img {src} class="pointer-events-none w-6 h-6 absolute top-[13.5rem] right-[2.5rem] md:right-[6rem] md:top-[15.5rem] xs:top-[15.5rem] sm:top-[13.6rem]" alt="sparkle.">
        <input bind:value={typed} class=" relative border-[#725AC1] border-2 rounded-full w-full bg-transparent p-2 px-6 pr-10 text-[#242038] capitalize md:p-5 md:pr-18" type="text" name="" id="" placeholder="I am living my best life..." >
        
    </label>
    <button on:click={addToList} type='submit' class="bg-[#725AC1] shadow-lg shadow-blue-900 rounded-md px-8 py-2 font-bold text-white mt-3 hover:bg-[#242038] ease-in-out duration-500">Add To List</button>
    
    
</div>

<div>
    {#if isEntered}
        <div class="flex items-center gap-1 mt-[4rem]" transition:blur>
        <h1 class="font-bold text-[1.3rem] capitalize" transition:blur>Ready to be sent to the <span class="text-[#725AC1]">Universe</span></h1>
        <img {src} class="w-6" alt="">
        </div>
    {:else}
        <div class="flex items-center gap-1 mt-[4rem]" transition:blur>
        <h1 class="font-bold text-[1.3rem] capitalize"  transition:blur>when youre ready to manifest type above <span class="text-[#725AC1]">and let the magic happen</span></h1>
        <img {src} class="w-6" alt="">
        </div>
    {/if}
    
    
        {#if isEntered}
        <button on:click= {releaseManifestation} class="bg-[#725AC1] p-3 rounded-md text-white font-semibold mt-4 hover:bg-[#281663] ease-in-out duration-700"  transition:blur>Release it all</button>
    {/if}

    <div  class="flex flex-col gap-6 mt-8">
        {#each manifestations as manifest}
        <div transition:blur class="bg-gradient-to-t from-[#CEBBD1] via-[#8D86C9] to-[#725AC1] p-8 rounded-md items-center flex gap-2 min-w-[1%]">
            <h2 class=" font-bold md:text-2xl capitalize text-white">{manifest}</h2>
            <img src={sparkly} class="w-6 h-6" alt="">

        </div>
        {/each}
    </div>

    

    
  
   
</div>


<style>
    :global(h2)
    {
        text-shadow: 0px 4px 14px #FFFFFF;
        word-wrap: break-word;
        word-break: break-all;
    }
</style>