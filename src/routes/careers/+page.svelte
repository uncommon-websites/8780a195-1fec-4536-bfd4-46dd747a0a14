<script lang="ts">
	// Types

	// Components
	import SectionHeader from "$lib/components/layout/SectionHeader.svelte";
	import Culture from "$lib/components/layout/Culture.svelte";
	import Testimonials from "$lib/components/layout/Testimonials.svelte";
	import SecondaryHero from "$lib/components/layout/hero-sections/SecondaryHero.svelte";
	import Card from "$lib/components/ui/Card.svelte";
	import JobList, { type JobOpening } from "./JobList.svelte";

	// Icons
	import IconBriefcase from "~icons/lucide/briefcase";
	import IconUsers from "~icons/lucide/users";
	import IconHeart from "~icons/lucide/heart";
	import IconGlobe from "~icons/lucide/globe";

	// Constants
	const SECTION_BASE_CLASSES = "section-py section-px container mx-auto";
	const GRADIENT_BG_CLASSES =
		"bg-gradient-to-br from-gray-50 to-gray-100 dark:from-gray-900 dark:to-gray-800";
	const ICON_CONTAINER_CLASSES =
		"bg-primary-50 text-primary-600 dark:bg-primary-950 dark:text-primary-400 flex items-center justify-center rounded-full";

	const benefits = [
  {
    title: "Unlimited primary care",
    description: "In-person and virtual doctor visits, 7 days a week, same-day access—no copays or waiting rooms.",
    icon: IconHeart
  },
  {
    title: "Zero-deductible & accident coverage",
    description: "We pay big bills over $500 and handle negotiation—your out of pocket is simple, predictable, and fully covered by your flexible health budget.",
    icon: IconBriefcase
  },
  {
    title: "Flexible health budget",
    description: "$300/month per employee, rolls over up to $3,300 a year. Use it for longevity, vision, dental, wearables, and more.",
    icon: IconUsers
  }
];

	const openings: JobOpening[] = [
		// Engineering
		{
			title: "Senior Frontend Developer",
			department: "Engineering",
			location: "Remote",
			type: "Full-time",
			url: "#"
		},
		{
			title: "Backend Engineer",
			department: "Engineering",
			location: "Remote",
			type: "Full-time",
			url: "#"
		},
		{
			title: "Design Engineer",
			department: "Engineering",
			location: "Remote",
			type: "Full-time",
			url: "#"
		},

		// Design
		{
			title: "UX/UI Designer",
			department: "Design",
			location: "Remote",
			type: "Full-time",
			url: "#"
		},
		{
			title: "Product Designer",
			department: "Design",
			location: "Remote",
			type: "Full-time",
			url: "#"
		},

		// Product
		{
			title: "Product Manager",
			department: "Product",
			location: "Remote",
			type: "Full-time",
			url: "#"
		},
		{
			title: "Product Analyst",
			department: "Product",
			location: "Remote",
			type: "Full-time",
			url: "#"
		},

		// Marketing
		{
			title: "Marketing Specialist",
			department: "Marketing",
			location: "Remote",
			type: "Full-time",
			url: "#"
		},
		{
			title: "Content Strategist",
			department: "Marketing",
			location: "Remote",
			type: "Full-time",
			url: "#"
		},
		{
			title: "Social Media Manager",
			department: "Marketing",
			location: "Remote",
			type: "Full-time",
			url: "#"
		}
	];

	const employeeTestimonials = [
  {
    name: "Michael Chen",
    position: "Senior Developer",
    company: "Engineering Team",
    quote:
      "At Rivendell, I’m trusted to solve real problems and given space to actually innovate. The culture here values curiosity and learning—everyone offers support when you need it, and you’re encouraged to take ownership beyond your job title. It’s the first company I’ve worked at where making things better for our members truly feels like a team passion, not just a mission statement.",
    image: "/generated/image-a-professional-asian-american-male-engin.webp"
  },
  {
    name: "Priya Sharma",
    position: "Product Designer",
    company: "Design Team",
    quote:
      "I joined Rivendell looking for real creative challenge, and stayed because I found so much more. Our team is refreshingly collaborative and every voice is heard, no matter your title. I’m constantly learning new skills and my ideas shape the product in visible ways. Plus, the flexibility and genuine care for well-being are unlike any place I’ve worked before.",
    image: "/generated/image-a-professional-south-asian-woman-designe.webp"
  },
  {
    name: "Marcus Johnson",
    position: "Marketing Lead",
    company: "Marketing Team",
    quote:
      "Rivendell’s leadership actually invests in my growth—be it mentorship, new responsibilities, or learning opportunities. The environment is open and inclusive, and there’s always room to try, fail, and succeed together. I’ve grown from a coordinator to a team lead in just a few years. It’s a rare mix of challenge and support that makes you excited for Mondays.",
    image: "/generated/image-a-professional-black-male-marketing-lead.webp"
  }
];


	const processSteps = [
  {
    step: 1,
    title: "Apply",
    description: "Send us your application and a brief note about what excites you about Rivendell."
  },
  {
    step: 2,
    title: "Intro call",
    description: "We schedule a short call to learn more about your experience and motivation."
  },
  {
    step: 3,
    title: "Team fit & work sample",
    description: "Spend time solving a real-world scenario with future teammates—async or live."
  },
  {
    step: 4,
    title: "Decision",
    description: "We let you know our decision within a week of your last conversation—honest, prompt communication guaranteed."
  }
];

	const values = [
  {
    icon: IconHeart,
    title: "Health-first mindset",
    description: "We don’t just build health plans—we actually care about your well-being and use our own benefit."
  },
  {
    icon: IconUsers,
    title: "Kindness with rigor",
    description: "We treat each other well while upholding a high bar for quality and thoughtful work."
  },
  {
    icon: IconBriefcase,
    title: "Bias for action",
    description: "We move quickly, learn fast, and expect ownership and initiative from everyone."
  },
  {
    icon: IconGlobe,
    title: "Collaborative impact",
    description: "We work cross-functionally and celebrate building meaningful, lasting products for teams."
  }
];
</script>

<!-- Hero Section -->

<SecondaryHero
	title="Redefine health. Empower small teams."
	subtitle="Build with a mission-driven team improving lives through care"
	imageSrc="/generated/image-a-diverse-startup-team-collaborating-in-.webp"
/>

<!-- Why Join Us Section -->
<section class={SECTION_BASE_CLASSES}>
	<SectionHeader title="Why join us?" subtitle="Build your career while making an impact" />

	<div class="mt-16 grid gap-4 md:grid-cols-3">
		{#each benefits as benefit}
			<Card {...benefit} />
		{/each}
	</div>
</section>

<!-- Culture Section -->
<Culture {values} />

<Testimonials testimonials={employeeTestimonials} />

<!-- Application Process -->
<section class={SECTION_BASE_CLASSES}>
	<div class="mx-auto">
		<h2 class="text-title1 mb-16">Our application process</h2>

		<div class="grid gap-12 md:grid-cols-3">
			{#each processSteps as { step, title, description }, i}
				<div class="flex flex-col">
					<div class="{ICON_CONTAINER_CLASSES} mb-6 size-11">
						<span class="text-headline">{step}</span>
					</div>
					<h3 class="text-headline mb-3">{title}</h3>
					<p class="text-body text-emphasis-low">{description}</p>
				</div>
			{/each}
		</div>
	</div>
</section>
<!-- Current Openings Section -->
<section class={GRADIENT_BG_CLASSES}>
	<div class="section-px section-py container mx-auto grid w-full items-start lg:grid-cols-2">
		<SectionHeader title="Current openings" subtitle="Find your perfect role" />

		<JobList {openings} />
	</div>
</section>
