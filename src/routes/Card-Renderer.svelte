<script lang="ts">
    import * as Card from "$lib/components/ui/card";
    export let item={
        src:"",
        desc:""
    }
  </script>
   
  <Card.Root >
    <Card.Header class=" !p-0  h-full" >
        <div style="background-image: url('{item.src}');     background-size: cover;"class="w-full rounded-t-lg h-32  md:h-40 "> 
        </div>
        <p class="md:text-sm text-xs text-gray-800 p-4">{item.desc}</p>
    </Card.Header> 
  </Card.Root>