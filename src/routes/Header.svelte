<script>
import { Button } from "$lib/components/ui/button"; 
	import * as Avatar from "$lib/components/ui/avatar";
    import { PlusSquare,Home ,AlignStartVertical,BookOpen,ChevronDown} from "lucide-svelte";
    
</script>

<header class={"items-center md:justify-between justify-around p-3 md:px-5 mx-2 md:mx-12 border-b-2 border-neutral-300 border-dotted"}> 
	<a class="relative px-3 md:m-0 text-neutral-900 font-medium font-sans " href="/">
	 <img class="h-7 w-7" src={"https://media.licdn.com/dms/image/D560BAQFHRBPTiTkqnA/company-logo_100_100/0/1687508146558/duggup_logo?e=1717632000&v=beta&t=xSqWU_IIJJTtXYzh2q7PTIulC5u7gsDwdq36CcPnU4U"} alt="">	
	 <span class="absolute text-lg top-0 left-12">duggup</span>
	</a>
	<nav class="flex items-center  px-5 gap-6"> 
		<ul class=" items-center hidden md:flex  gap-2">
			<Button variant="ghost" class="text-neutral-500 p-2 flex gap-1  items-center" href="/"><Home size={18}/> <span>Home</span></Button>
			<Button variant="ghost" class="text-neutral-500 p-2 flex gap-1  items-center" href="/"><AlignStartVertical size={18}/> <span>Home</span></Button>
			<Button variant="ghost" class="text-neutral-500 p-2 flex gap-1  items-center" href="/"><BookOpen size={18}/> <span>Home</span></Button>
		</ul>
		<Button  size="sm" variant="thick" class="mx-4 justify-between md:flex items-center !hidden gap-5 !px-5">
  <PlusSquare strokeWidth={1.5}  size={18}/>
			Post</Button>
		<Button  class="flex flex-col md:flex-row !px-5 md:px-8 items-center md:gap-4" size="lg" variant="ghost">
			<Avatar.Root>
				<Avatar.Image class="border-2 border-neutral-200 rounded-full" src="https://media.licdn.com/dms/image/D4E03AQF-fLP5TtdtOQ/profile-displayphoto-shrink_200_200/0/1677089436637?e=1715212800&v=beta&t=RSHmTl4pQ-_Jb_0bp60VG8ZykohknsCVYRAquHMLa7c" alt="Avatar" />
				<Avatar.Fallback>Avatar</Avatar.Fallback>
			  </Avatar.Root>
			<spna class="flex gap-1 items-center text-base text-muted-foreground ">Krishna Kiran 
			<ChevronDown size={14}/>
			</spna> 
		</Button>
	</nav>
 
	
</header>
<style>
	header {
		display: flex;
		justify-content: space-between;
	} 
	ul {
		position: relative;
		padding: 0;
		margin: 0;
		height: 3em;
		 
		justify-content: center;
		align-items: center;
		list-style: none;
		background: none; 
	} 
 
</style>
