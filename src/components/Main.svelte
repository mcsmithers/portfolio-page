<script>
	import Step from './Step.svelte';

	let steps = [
		{ name: 'Pawsitively Yours', icon: 'fa-solid fa-paw' },
		{ name: 'Pet Report', icon: 'fa-solid fa-camera' },
		{ name: 'Botanical Bites Backend', icon: 'fa-solid fa-cookie-bite' }
	];

	let benefits = [
		{
			name: 'An enthusiastic, dedicated developer',
			description:
				'I learned programming through a combination f education and experience through the University of Utah and Georgia Institute of Technology.  I got into programming through GIS by playing with queries and Python and the test was history.  The creativity and problem-solving to deliver elegance and excellence are what get me on my machine in the mornings.  My main expertise is in JavaScript its frameworks and my skills continue to grow and evolve with each project.  My skills are evolving into cloud services, design, backend, UI/UX, and much more.'
		},
		{
			name: 'An analyst who can speak both tech and business',
			description:
				'As a former GIS practitioner, I love to dive into data and turn it into meaningful information through articulate yet simple visuals and a great sense of holistic knowledge to solve business needs.'
		},
		{
			name: 'A tech writer who can make complexity into simplicty',
			description:
				'I delight in researching and explaining things to anyone.  I use visuals, clear communication, and careful planning as I document technical ideas.'
		}
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
				class="blueShadow mx-auto lg:mr-auto lg:ml-0 text-base sm:text-lg md:text-xl poppins relative overflow-hiddenpx-6 py-3 group rounded-full bg-white text-slate-950 cursor-pointer"
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
					Pawsitively Yours is a petcare application being created with <strong
						class="text-violet-400"
						>React.js + NEXT.js + Node.js + Stripe + Docker + TailwindCSS + PostgresSQL + NextAuth +
						Prisma</strong
					> Stripe is used for all transaction handling.
				</p>
			</Step>
			<Step step={steps[1]}>
				<p>
					Pet Report is a <strong
						class="text-violet-400">Python</strong
					> project that takes images and turnt them into a PDF like you would want from a pet sitter maybe.
				</p>
			</Step>
			<Step step={steps[2]}>
				<p>
					Botanical Bites Backend is a gastronomy application being created with <strong
						class="text-violet-400">NEXT.js + Node.js</strong
					>
				</p>
			</Step>
		</div>
	</section>

	<section
		id="about"
		class="py-20 pt-20 lg:pt-16 lg:py-32 flex flex-col gap-16 sm:gap-20 md:gap-24 relative"
	>
		<div
			class="flex flex-col gap-2 text-center relative before:absolute before:top-0 before:left-0 before:w-2/3 before:h-1.5 before:bg-violet-700 after:absolute after:bottom-0 after:right-0 after:w-2/3 after:h-1.5 after:bg-violet-700 py-4"
		>
			<h6 class="text-lg sm:text-xl md:text-2xl">Want to know more?</h6>
			<h3 class="font-semibold text-3xl sm:text-4xl md:text-5xl">
				A bit <span class="poppins text-violet-400">about </span>me
			</h3>
		</div>
		<p class="mx-auto poppins font-semibold text-lg sm:text-xl md:text-2xl">I am . . .</p>
		<div class="flex flex-col gap-20 w-full mx-auto max-w-[800px]">
			{#each benefits as benefit, index}
				<div class="flex gap-6 sm:gap-8">
					<p class="poppins text-4xl sm:text-5xl md:text-6xl text-slate-500 font-semibold">
						0{index + 1}
					</p>
					<div class="flex flex-col gap-6 sm:gap-8">
						<h3 class="text-2xl sm:text-3xl md:text-5xl">{benefit.name}</h3>
						<p>{benefit.description}</p>
					</div>
				</div>
			{/each}
		</div>
		<h5 class="text-2xl sm:text-3xl font-semibold text-center poppins">The <span class="text-violet-400 poppins">Complete </span>Package</h5>
		<div class="flex flex-col overflow-x-scroll gap-10 ma-w-[800px] mx-auto w-full">
			<table class="bg-white text-slate-700 rounded text-center">
				<thead class="border-b border-solid border-slate-200">
					<tr class="">
						<th />
						<th class="whitespace-nowrap p-2 px-4">Candidate A</th>
						<th class="whitespace-nowrap p-2 px-4">Candidate B</th>
						<th class="whitespace-nowrap p-2 px-4">Candidate C</th>
						<th class="whitespace-nowrap bg-violet-700 p-4 px-8 text-white">Me</th>
					</tr>
				</thead>
				<tbody>
					<tr class="border-b border-solid border-slate-200">
						<td class="border-r border-solid border-white pl-4 pr-8 py-4 font-semibold text-sm whitespace-nowrap"
							>Enthusiasm
						</td>
						<td><i class="fa-solid fa-xmark text-slate-500"></i></td>
						<td><i class="fa-solid fa-check text-slate-500"></i></td>
						<td><i class="fa-solid fa-check text-slate-500"></i></td>
						<td><i class="fa-solid fa-check text-green-500"></i></td>
					</tr>
                    <tr class="border-b border-solid border-slate-200">
						<td class="border-r border-solid border-white pl-4 pr-8 py-4 font-semibold text-sm whitespace-nowrap"
							>Dedication
						</td>
						<td><i class="fa-solid fa-xmark text-slate-500"></i></td>
						<td><i class="fa-solid fa-check text-slate-500"></i></td>
						<td><i class="fa-solid fa-xmark text-slate-500"></i></td>
						<td><i class="fa-solid fa-check text-green-500"></i></td>
					</tr>
                    <tr class="border-b border-solid border-slate-200">
						<td class="border-r border-solid border-white pl-4 pr-8 py-4 font-semibold text-sm whitespace-nowrap"
							>Trusted Teammate
						</td>
						<td><i class="fa-solid fa-check text-slate-500"></i></td>
						<td><i class="fa-solid fa-xmark text-slate-500"></i></td>
						<td><i class="fa-solid fa-xmark text-slate-500"></i></td>
						<td><i class="fa-solid fa-check text-green-500"></i></td>
					</tr>
                    <tr class="border-b border-solid border-slate-200">
						<td class="border-r border-solid border-white pl-4 pr-8 py-4 font-semibold text-sm whitespace-nowrap"
							>Critical Thinker
						</td>
						<td><i class="fa-solid fa-xmark text-slate-500"></i></td>
						<td><i class="fa-solid fa-xmark text-slate-500"></i></td>
						<td><i class="fa-solid fa-xmark text-slate-500"></i></td>
						<td><i class="fa-solid fa-check text-green-500"></i></td>
					</tr>
                    <tr class="border-b border-solid border-slate-200">
						<td class="border-r border-solid border-white pl-4 pr-8 py-4 font-semibold text-sm whitespace-nowrap"
							>Always Evolving
						</td>
						<td><i class="fa-solid fa-xmark text-slate-500"></i></td>
						<td><i class="fa-solid fa-xmark text-slate-500"></i></td>
						<td><i class="fa-solid fa-xmark text-slate-500"></i></td>
						<td><i class="fa-solid fa-check text-green-500"></i></td>
					</tr>
				</tbody>
			</table>
		</div>
        <div class="mx-auto -mt-12 italic sm:hidden opacity-50">
            <p>Scroll to se more &rarr;</p>
        </div>
        <p class="mx-auto">So why not invest in me?</p>
	</section>
</main>
