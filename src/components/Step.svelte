<script>
    export let step;
</script>
<a href="{step.href}" target="_blank">
<div class="w-full h-70 bg-violet-600 duration-200 rounded-2xl p-3 my-1 hover:bg-slate-950">
    <h1 class="tradewind text-center text-2xl lg:text-3xl text-white">
        {step.name}
    </h1>
    <div class="flex gap-1 sm:gap-10 p-2 sm:p-5">
        <img
            src={step.icon}
            alt="project"
            class="w-30 h-30 left-0"
        />
        <h3 class="text-xl lg:text-2xl">
            {step.desc}
        </h3>
    </div>
    <div class="flex gap-2 my-2 md:mx-45">
        <button class="rounded-full bg-amber-50 text-slate-950 p-3">{step.lang}</button>
    </div>
</div>
</a>