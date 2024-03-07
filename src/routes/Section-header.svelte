  <script>
   	import * as Avatar from "$lib/components/ui/avatar"; 
   import { Button } from "$lib/components/ui/button";
   import {ExternalLink ,MoreHorizontal} from 'lucide-svelte'
  </script>

  <div class="flex md:flex-row flex-col md:items-start mx-5 md:mx-24 items-center justify-center md:justify-between">
    <div class="flex flex-col items-center justify-between">
        <Avatar.Root  class="h-32 w-32">
            <Avatar.Image class="border-[3px] border-neutral-200 rounded-full" src="https://media.licdn.com/dms/image/D4E03AQF-fLP5TtdtOQ/profile-displayphoto-shrink_200_200/0/1677089436637?e=1715212800&v=beta&t=RSHmTl4pQ-_Jb_0bp60VG8ZykohknsCVYRAquHMLa7c" alt="Avatar" />
            <Avatar.Fallback>Avatar</Avatar.Fallback>
        </Avatar.Root>
        <span class="text-2xl p-2 ml-2 text-muted-foreground font-semibold">Krishna <span class="ml-2">
            Kiran </span>
        </span>
    </div>
    <div class="flex py-12 md:px-6  flex-col gap-6 md:items-start items-center  md:justify-between">
    <p class="text-sm md:text-base">
        Co-Founder and CEO at Duggup - Social network for people in tech. Ex-Amazon Head of Engineering. I write hot-takes on building a business, shipping delightful products and accelerating product and career growth.
    </p>
    <Button  size="lg" variant="thick" class="mx-4 justify-between items-center flex gap-5">Followed</Button>
</div>

    <div class="md:flex hidden w-[30%] p-12 !px-0 flex-col items-end">
	 <img class="rounded-full w-10" src={"https://media.licdn.com/dms/image/D560BAQFHRBPTiTkqnA/company-logo_100_100/0/1687508146558/duggup_logo?e=1717632000&v=beta&t=xSqWU_IIJJTtXYzh2q7PTIulC5u7gsDwdq36CcPnU4U"} alt="">	 
    <span class="text-lg text-semibold">Duggup</span>
    <span class="text-sm text-muted-foreground whitespace-nowrap">Co-Founder and CEO </span>
    <a class="flex text-muted-foreground justify-center items-center gap-2 text-sm my-5" href="/">My website <ExternalLink size={16}/> <MoreHorizontal size={16}/> </a>
    </div>
  </div>