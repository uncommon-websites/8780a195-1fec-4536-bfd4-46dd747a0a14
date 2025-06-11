<script lang="ts">
	// Components
	import CallToAction from "$lib/components/layout/CallToAction.svelte";

	// Icons
	import StakeholderGrid from "$lib/components/layout/StakeholderGrid.svelte";
	import Story from "./Story.svelte";
	import SecondaryHero from "$lib/components/layout/hero-sections/SecondaryHero.svelte";
	import Culture from "$lib/components/layout/Culture.svelte";

	// Constants
	const values = [
		{
			title: "Innovation",
			description: "Constantly challenging the status quo to create better solutions."
		},
		{
			title: "Integrity",
			description: "Building trust through transparent actions and honest communication."
		},
		{
			title: "Impact",
			description: "Measuring our success by the positive change we create for our clients."
		}
	];
</script>

<SecondaryHero
  title="Better health benefits for startups"
  subtitle="Unlimited primary care, zero deductibles, and $300 monthly health spend—simple pricing, no surprises"
  imageSrc="/generated/image-a-diverse-group-of-startup-team-members-.webp"
/>

<!-- Story Section -->
<Story
	paragraphs={[
		"We started Rivendell after struggling to find health benefits that actually worked for our own startup teams. Everything was either outdated, overloaded with fine print, or designed for giant corporations. We talked to dozens of founders facing the same issue—burning cash on plans their employees rarely used, or skipping coverage entirely and hoping for the best. It didn’t sit right with us.",
		"So we built a health plan designed specifically for startups. Something clear, proactive, and built around what employees really need: unlimited access to primary care, preventative tools that help them stay ahead of issues, and accident coverage that doesn’t come with scary bills. No red tape, no guessing, just one easy-to-manage plan with built-in support and predictable pricing.",
		"What makes Rivendell different is what we've included—and what we’ve left out. There are no deductibles and no surprises. Every employee gets a monthly health budget to spend how they want—on rings, beds, therapy, dental, and more. We use real diagnostics to support long-term health and longevity, and if something major happens, we negotiate the bills so your employees don’t have to. We're building health benefits that teams use, value, and trust—because startups deserve better."
	]}
/>

<!-- Our Culture Section -->
<Culture />

<!-- StakeholderGrid Section -->
<StakeholderGrid
  stakeholderType="team"
  title="Our team."
  subtitle="The people building Rivendell."
  stakeholders={[
    {
      name: "David Wilson",
      position: "Co-Founder & CEO",
      bio: "Purposeful leader rethinking healthcare for modern teams.",
      image: "/generated/image-headshot-portrait-of-a-confident-male-st.webp"
    },
    {
      name: "Jessica Hayes",
      position: "Co-founder & COO",
      bio: "Operational architect turning complexity into effortless care.",
      image: "/generated/image-headshot-portrait-of-a-smiling-female-st.webp"
    },
    {
      name: "Constanza Perez",
      position: "Head of Product",
      bio: "Designs proactive health experiences employees love to use.",
      image: "/generated/image-headshot-portrait-of-a-female-product-le.webp"
    },
    {
      name: "Meera Desai",
      position: "Head of Engineering",
      bio: "Builds secure, seamless systems for smarter healthcare.",
      image: "/generated/image-headshot-portrait-of-a-female-engineerin.webp"
    },
    {
      name: "Benjamin Weber",
      position: "Backend Engineer",
      bio: "Makes health data work for the people it serves.",
      image: "/generated/image-headshot-portrait-of-a-thoughtful-male-b.webp"
    },
    {
      name: "Jacob Jones",
      position: "Frontend Engineer",
      bio: "Crafts interfaces that make health benefits actually usable.",
      image: "/generated/image-headshot-portrait-of-a-cheerful-male-fro.webp"
    },
    {
      name: "Maria Rodrigues",
      position: "Product Designer",
      bio: "Turns care journeys into intuitive digital experiences.",
      image: "/generated/image-headshot-portrait-of-a-creative-female-p.webp"
    }
  ]}
/>


<StakeholderGrid
	stakeholderType="investor"
	title="Backed by the best."
	subtitle="Point Nine, TSIC and others"
	stakeholders={[
		{
			name: "Point Nine Capital",
			image: "https://cdn.brandfetch.io/pointnine.com/w/400/h/400/logo?c=1id_elLz2Bd5Ej-dWo7"
		},
		{
			name: "TSIC Ventures",
			image: "https://cdn.brandfetch.io/tiny.vc/w/400/h/400/logo?c=1a2b3c4d5e"
		},
		{
			name: "Sequoia Capital",
			image: "https://cdn.brandfetch.io/sequoiacap.com/w/400/h/400/logo"
		}
	]}
/>

<!-- CTA Section -->
<CallToAction
	title="Let’s rethink health benefits for startups"
	subtitle="Ready to put health first?"
	description="Get in touch to join the Rivendell waitlist, connect with our sales team, or apply for open roles. We’re building health plans that actually work for startups—making wellbeing real, affordable, and simple. Email sales@rivendell.health, join the waitlist, or explore careers—your team’s better benefits start here."
	callsToAction={[
	  { href: 'mailto:sales@rivendell.health', label: 'Contact sales', variant: 'secondary' },
	  { href: '/waitlist', label: 'Join the waitlist', variant: 'primary' },
	  { href: '/careers', label: 'Explore careers', variant: 'tertiary' },
	]}
/>
