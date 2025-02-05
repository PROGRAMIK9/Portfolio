<script>
    import Footer from "./Footer.svelte";

    export let y;
    let nav = [
        {name:"Project",link:"#project"},
        {name:"About",link:"#about"}
    ]
</script>

<header class={"flex w-full items-center justify-between sticky z-[10] top-0 left-0 duration-200 px-1 border border-solid " + (
    y>0?'py-4 bg-slate-950 border-violet-950':'py-6 bg-transparent border-transparent'
)}>
    <h1 class="text-2xl px-4">
        <b class="tradewind">Aaryamann</b> Prabhu
    </h1>
    <div class="sm:flex gap-5 text-2xl items-center hidden px-4">
        {#each nav as item,index}
            <a class = "duration-200 hover:text-violet-500" href='{item.link}'>
                <p>{item.name}</p>
            </a>
        {/each}   
        <a href="#contact" class="blueshadow relative overflow-hidden  py-2 px-5 group rounded-full bg-white text-slate-950">
            <div class=" absolute top-0 right-full w-full h-full bg-violet-400 opacity-20 group-hover:translate-x-full z-0 duration-200"></div>
                <h4 class="relative z-9">Get in Touch</h4>
        </a>
    </div>
       
</header>
