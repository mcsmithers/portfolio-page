<script>
    export let y;

    let tabs =[
        {name: 'Projects', link: '#projects'},
        {name: 'About Me', link: '#about'},
    ];

</script>

<header class={'sticky z-[10] top-0 duration-200 px-6 flex items-center justify-between border border-solid ' + (
    y > 0 ? 'py-4 bg-slate-950 border-violet-950' : ' py-6 bg-transparent border-transparent'
)}>
	<h1 class="font-medium">
		<b class="font-bold poppins">Christina</b> Smithers
	</h1>
	<div class="sm:flex ml-auto pr-4 items-center gap-4 hidden">
		{#each tabs as tab, index}
			<a class="duration-200 hover:text-violet-400" href={tab.link}>
				<p>{tab.name}</p>
			</a>
		{/each}
	</div>
    <a class="blueShadow relative overflow-hidden px-5 py-2 group rounded-full bg-white text-slate-950" href="https://linkedin.com/in/in/christinasmithers" target="_blank">
        <div class="absolute top-0 right-full w-full h-full bg-violet-400 opacity-20 group-hover:translate-x-full z-0 duration-200"/>
        <h4 class="relative z-9">Get In Touch</h4>
    </a>
</header>
