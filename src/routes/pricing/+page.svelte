<script lang="ts">
	// Types
	import type { PageProps } from "./$types";

	// Components
	import Features from "$lib/components/layout/Features.svelte";
	import Testimonials from "$lib/components/layout/Testimonials.svelte";
	import CallToAction from "$lib/components/layout/CallToAction.svelte";
	import Pricing from "$lib/components/layout/Pricing.svelte";

	// Props
	const { data }: PageProps = $props();
</script>

<Pricing />

<Testimonials
  testimonials={[
    {
      name: "Maya Lin",
      position: "Head of People",
      company: "Optima Robotics",
      quote:
        "Our team gets quick access to care, actual direction on health goals, and budget flexibility they love—all without insurance headaches.",
      image:
        "/generated/image-a-professional-headshot-of-an-asian-woma.webp"
    },
    {
      name: "Erik Salazar",
      position: "Engineering Manager",
      company: "NeuronCore",
      quote:
        "The DNA and blood test combo helped me catch health trends before they became issues. This is what real preventive care should look like.",
      image:
        "/generated/image-a-professional-headshot-of-a-latino-man-.webp"
    },
    {
      name: "Delia Voigt",
      position: "Ops Lead",
      company: "Parseworks",
      quote:
        "Negotiating large bills? Rivendell handled everything. I paid a flat copay, and they handled the rest—saved me thousands.",
      image:
        "/generated/image-a-professional-headshot-of-a-white-woman.webp"
    }
  ]}
/>

<CallToAction
  title="Better health benefits. Without the headaches."
  subtitle="A plan your team will actually use"
  description="Rivendell gives startups and small teams access to high-quality care, proactive health tracking, and generous coverage — all under one simple plan. Our Startup Health Plan is $1,000 per employee per month — no extra fees, no hidden costs. Set your team up with a plan they'll thank you for."
  imageSrc="/generated/image-a-happy-startup-employee-in-a-modern-off.webp"
  callsToAction={[
    { href: 'mailto:sales@rivendell.health', label: 'Contact sales', variant: 'primary' },
    { href: '/waitlist', label: 'Join the waitlist', variant: 'secondary' }
  ]}
/>
