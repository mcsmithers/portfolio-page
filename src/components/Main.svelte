<script>
	import Step from './Step.svelte';

	let steps = [
		{ name: 'Pawsitively Yours', icon: 'fa-solid fa-paw' },
		{ name: 'Botanical Bites', icon: 'fa-solid fa-plant-wilt' },
		{ name: 'Botanical Bites Backend', icon: 'fa-solid fa-cookie-bite' }
	];
</script>

<main class="flex flex-col flex-1 p-4">
	<section id="introPage" class="grid grid-cols-1 lg:grid-cols-2 gap-10 py-8 sm:py-14">
		<div class="flex flex-col lg:justify-center text-center lg:text-left gap-6 md:gap-8 lg:gap-10">
			<h2 class="font-semibold text-4xl sm:text-5xl md:text-6xl">
				Hi! I'm <span class="poppins text-violet-400">Christina</span> Smithers <br /> Full Stack
				<span class="poppins text-violet-400">Developer</span>
			</h2>
			<p class="text-base sm:text-lg md:text-xl">
				My <span class="text-violet-400">favorite tech</span> includes JavaScript (NEXT.JS, React.js,
				or Sveltekit), TailwindCSS, Node.js & PostgresSQL!
			</p>
			<a
				class="blueShadow mx-auto lg:mr-auto text-base sm:text-lg md:text-xl poppins relative overflow-hiddenpx-6 py-3 group rounded-full bg-white text-slate-950 cursor-pointer"
				href="https://linkedin.com/in/christinasmithers"
				target="_blank"
			>
				<div
					class="absolute top-0 right-full w-full h-full bg-violet-400 opacity-20 group-hover:translate-x-full z-0 duration-200"
				/>
				<h4 class="relative z-9">Get In Touch &rarr;</h4>
			</a>
		</div>
		<div class="relative shadow-2xl grid place-items-center">
			<img
				src={'images/profile.JPEG'}
				alt="Profile image"
				class="object-cover z-[2] max-h-[70vh]"
			/>
		</div>
	</section>

	<section id="projects" class="py-20 lg:py-32 flex flex-col gap-24">
		<div class="flex flex-col gap-2 text-center">
			<h6 class="text-lg sm:text-xl md:text-2xl">A few of my creative endeavors.</h6>
			<h3>Curious to <span class="poppins text-violet">see </span>some of my work?</h3>
		</div>
		<a
			href="https://github.com/mcsmithers"
			target="_blank"
			class="mx-auto px-4 py-2 rounded-md border border-solid border-white flex items-center gap-2 -mb-4 sm:mb-0 -mt-10 hover:border-violet-700 duration-200"
		>
			<i class="fa-regular fa-heart"></i>
			<p>Projects in my freetime</p>
		</a>
		<div class="grid grid-cols-1 lg:grid-cols-3 gap-12 lg:gap-10">
			<Step step={steps[0]}>
				<p>
					Pawsitively Yours is a petcare application being created with <strong class="text-violet-400"
					>React.js + NEXT.js + Node.js + Stripe + Docker + TailwindCSS + PostgresSQL + NextAuth + Prisma</strong> Stripe is used for all transaction handling.
				</p>
			</Step>
			<Step step={steps[1]}>
				<p>
					Botanical Bites is application for culinary arts created with <strong
						class="text-violet-400"
					>React.js + NEXT.js + Gatsby.js</strong>  Gatsby.js is used for content
				</p>
			</Step>
			<Step step={steps[2]}>
				<p>
					Botanical Bites Backend is a gastronomy application created with <strong
						class="text-violet-400"
					>NEXT.js + Node.js</strong>
				</p>
			</Step>
		</div>
	</section>
</main>
