<script>
    import CardRenderer from "../../../../routes/Card-Renderer.svelte";
     import {items} from '../../.././data.js';
</script>

 
    <div class="flex justify-between flex-col md:py-10 ">
            {#each items as item,i(i)} 
       <div class="flex">
        <div class="flex relative items-center px-4 justify-end md:w-[14%] w-[30%]">
             {#if item.timeline}
             <p class="text-sm  text-muted-foreground">{item.timeline}</p>
             {:else if item.detail}
             <div class="flex flex-col  justify-end items-end">
                <img class="md:w-12 md:h-12 h-6 w-6 rounded-full mb-2" src={item.detail.icon} alt="">
                 <h2 class="md:text-xl relative font-semibold"> 
                     {item.detail.title}
                    </h2>
                    <p class="md:text-sm text-xs text-muted-foreground whitespace-nowrap">{item.detail.location}</p> 
                    <p class="md:text-sm text-xs  text-muted-foreground">Joined</p> 
                    <p class="md:text-sm text-xs  text-muted-foreground">{item.detail.time}</p> 
                </div>
             {/if}

           </div>
            <div class="md:w-[12%] w-[15%] flex items-center border-l-2 border-dotted ">
               {#if !item.data}
               <span class=" flex items-center justify-center h-6 w-6 -ml-3 bg-sky-600 rounded-full">
                <span class="bg-white block rounded-full h-2 w-2"></span> 
            </span>
            {:else}
            <span class=" flex items-center justify-center h-4 w-4 -ml-2 bg-sky-600 rounded-full">
                <span class="bg-white block rounded-full h-2 w-2"></span></span>
            {/if}
            </div>
            {#if item.data }
            <div class="md:w-[70%] w-[55%] grid md:grid-cols-2 my-6 gap-5">
                           {#each item.data as data}
                           <CardRenderer item={data} />
                           {/each}  
           </div>
            {:else}
            <div class="flex flex-col justify-center  h-[20vh]">
                <h2 class="text-xl my-2 relative font-semibold"> 
                    {item.title}
                </h2>
                <p class="text-sm text-muted-foreground">{item.subtitle}</p>
            </div>
            {/if}
       </div>
       {/each} 
        </div>  