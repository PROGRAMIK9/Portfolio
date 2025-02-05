<script>
    import Step from "./Step.svelte";
    let benefits = [
        {
            metric: "10x",
            name: "a self taught developer",
            description:
                "I learnt coding as i loved to solve problems and face the challenge of the computers. I am dedicated and always up for a challenge!",
        },
        {
            name: "a sucker for learning new things",
            description:
                "I love learning new things and will always love to try something different. I will explore the languages my way and try to be the best at it.",
        },
        {
            name: "a good communicator",
            description:
                "Communication is key and I believe in communicating my flaws as well as strengths to ensure we are on the same page. ",
        },
    ];
    let steps = [
        {
            name: "Spotify Clone",
            href: "https://github.com/PROGRAMIK9/Spotify_Clone-Aaryamann-",
            icon: "images/spotify.png",
            desc: "A Spotify Clone. Listen to Music,Create Playlists and more!",
            lang: "MERN",
        },
        {
            name: "TO-DO-List",
            href: "https://github.com/PROGRAMIK9/CODSOFT_TODO",
            icon: "images/to-do.png",
            desc: "Create Tasks,Mark them As complete with local persistence!",
            lang: "Kotlin",
        },
        {
            name: "Quote Generator",
            href: "https://github.com/PROGRAMIK9/CodSoft_QuoteApp",
            icon: "images/quotes.png",
            desc: "Generate a New Quote!Share it and add it to your favourites!",
            lang: "Kotlin",
        },
    ];
</script>

<main class="flex flex-col flex-1 p-4">
    <section
        id="intro"
        class="grid grid-cols-1 lg:grid-cols-2 gap-10 px-8 sm:py-14"
    >
        <div
            class="flex flex-col text-center my-auto lg:justify-center lg:text-left gap-6 md:gap-8 lg:gap-10"
        >
            <h2
                class="font-semibold text-center text-3xl sm:text-4xl md:text-5xl"
            >
                Hii! I am <span class="tradewind text-violet-400"
                    >Aaryamann Prabhu.</span
                ><br /> I am a final year CS Student and a<span
                    class="tradewind text-violet-400">Web Dev Intern</span
                > at Medblocks.
            </h2>
            <a
                href="#contact"
                class="blueshadow relative overflow-hidden mx-auto text-center text-base sm:text-lg md:text-xl py-2 px-5 group rounded-full bg-white text-slate-950"
            >
                <div
                    class=" absolute top-0 right-full w-full h-full bg-violet-400 opacity-20 group-hover:translate-x-full z-0 duration-200"
                ></div>
                <h4 class="relative z-9">Get in Touch &rarr;</h4>
            </a>
        </div>
        <div class="relative shadow-2xl grid place-items-center">
            <img
                src={"images/unnamed.jpg"}
                alt="My pic"
                class="rounded-3xl h-[70vh] z-[2] object-cover"
            />
        </div>
    </section>
    <section
        id="project"
        class="py-20 my-20 sm:my-0 lg:py-30 flex flex-col gap-24"
    ><div
    class="flex flex-col gap-2 text-center relative before:absolute before:top-0 before:left-0 before:w-2/3 before:h-1.5 before:bg-violet-700 after:absolute after:bottom-0 after:right-0 after:w-2/3 after:h-1.5 after:bg-violet-700 py-4"
>
        <div class="flex flex-col gap-2">
            <h6 class="tradewind text-2xl sm:text-3xl md:text-4xl">
                My Projects!
            </h6>
        </div>
    </div>
        <div class="grid grid-cols-1 sm:grid-cols-3 sm:gap-3">
            <Step step={steps[0]} />
            <Step step={steps[1]} />
            <Step step={steps[2]} />
        </div>
    </section>
    <section
        id="about"
        class="py-20 pt-10 lg:pt-16 lg:py-32 flex flex-col gap-16 sm:gap-20 md:gap-24 relative"
    >
        <div
            class="flex flex-col gap-2 text-center relative before:absolute before:top-0 before:left-0 before:w-2/3 before:h-1.5 before:bg-violet-700 after:absolute after:bottom-0 after:right-0 after:w-2/3 after:h-1.5 after:bg-violet-700 py-4"
        >
            <h6 class="text-large sm:text-xl md:text-2xl">
                Want to know more?
            </h6>
            <h3 class="font-semibold text-3xl sm:text-4xl md:text-5xl">
                A bit <span class="poppins text-violet-400">about</span> me.
            </h3>
        </div>
        <p class="mx-auto font-semibold text-lg sm:text-xl md:text-2xl">
            I am . . .
        </p>
        <div class="flex flex-col gap-20 w-full mx-auto max-w-[800px]">
            {#each benefits as benefit, index}
                <div class="flex gap-6 sm:gap-8">
                    <p
                        class="tradewind text-4xl sm:text-5xl md:text-6xl text-slate-500 font-semibold"
                    >
                        0{index + 1}
                    </p>
                    <div class="flex flex-col gap-6 sm:gap-8">
                        <h3 class="text-2xl sm:text-3xl md:text-5xl">
                            {benefit.name}
                        </h3>
                        <p>{benefit.description}</p>
                    </div>
                </div>
            {/each}
        </div>
    </section>
</main>
