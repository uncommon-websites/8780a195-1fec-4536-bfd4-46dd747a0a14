<script lang="ts">
	// Components
	import UseCases from "$lib/components/layout/UseCases.svelte";
	import Summary from "$lib/components/layout/Summary.svelte";
	import Features from "$lib/components/layout/Features.svelte";
	import Testimonials from "$lib/components/layout/Testimonials.svelte";
	import CallToAction from "$lib/components/layout/CallToAction.svelte";
	import AboutTeaser from "$lib/components/layout/AboutTeaser.svelte";
	import LogoScroller from "$lib/components/layout/LogoScroller.svelte";
	import CustomerCardHero from "$lib/components/layout/hero-sections/CustomerCardHero.svelte";
</script>

<CustomerCardHero
    centered={true}
    title="Health benefits your team will actually use"
    subtitle="Unlimited primary care, zero-deductible coverage, personalized longevity tools, and a flexible health budget—all in one simple plan for startups."
    customers={[
        {
            name: "Emily Chen",
            position: "Founder, LemonTree Labs",
            imageSrc: "/generated/image-a-young-female-founder-sits-confidently-.webp"
        },
        {
            name: "Michael Ruiz",
            position: "CTO, Orbit Analytics",
            imageSrc: "/generated/image-a-middle-aged-male-cto-is-smiling-warmly.webp"
        },
        {
            name: "Gabriela Torres",
            position: "Product Manager, Vela Tech",
            imageSrc: "/generated/image-a-young-hispanic-woman-product-manager-s.webp"
        },
        {
            name: "Theo Williams",
            position: "HR Manager, Vertex Co.",
            imageSrc: "/generated/image-a-black-male-hr-manager-poses-in-a-relax.webp"
        },
        {
            name: "Lucy Kim",
            position: "Engineer, Nova Health",
            imageSrc: "/generated/image-an-asian-female-engineer-is-positioned-i.webp"
        }
    ]}
/>
<LogoScroller
  label="Trusted by fast-growing startups"
  logoUrls={[
    'https://logo.clearbit.com/fivetran.com',
    'https://logo.clearbit.com/linear.app',
    'https://logo.clearbit.com/webflow.com',
    'https://logo.clearbit.com/vanta.com'
  ]}
/>

<Summary
	generating
	title="What we do"
	text="Our technology delivers measurable results through secure, adaptable solutions that directly increase productivity and drive growth."
/>

<Testimonials
	testimonials={[
		{
			name: "Sofia Mendez",
			position: "Founder",
			company: "Brightspace AI",
			quote:
				"Rivendell cut our admin time by at least 20 hours a month. Signing up took less than a day, and everything integrates with payroll. That’s time I can now spend actually growing the business.",
			image: "/generated/image-a-young-latina-woman-startup-founder-smi.webp"
		},
		{
			name: "Terrence Hall",
			position: "COO",
			company: "Atlas Robotics",
			quote:
				"One of our engineers got hurt biking to work. Five minutes later, he texts me that Rivendell already handled the claim. No forms, no stress, and no surprise bills. That gave us real peace of mind.",
			image: "/generated/image-a-middle-aged-black-man-a-business-execu.webp"
		},
		{
			name: "Grace Lin",
			position: "Finance Manager",
			company: "NextLeap Solutions",
			quote:
				"We saved over $8,400 in potential out-of-pocket costs last quarter alone—mostly due to Rivendell’s bill negotiation and flexible budget. Our team actually uses it, and finance loves the ROI.",
			image: "/generated/image-an-asian-woman-finance-manager-reviewing.webp"
		}
	]}
/>

<Features
	title="Why startups choose Rivendell"
	subtitle="Comprehensive health, whole-team simplicity, and control of every dollar. Here’s what makes us different."
	features={[
		{
			title: "Primary care without limits",
			description: "Your team can access trusted providers every day, not just when something goes wrong. No delays, no gatekeeping."
		},
		{
			title: "Zero-deductible, cost-capped coverage",
			description: "We handle bills over $500 directly. You pay one simple copay, which can be covered by your monthly health budget."
		},
		{
			title: "Clear path to long-term health",
			description: "Quarterly blood panels and medical-grade DNA testing give every employee a baseline and personal health plan from day one."
		},
		{
			title: "We handle the big bills for you",
			description: "When unexpected costs hit, we step in. We negotiate, cover, and pay—often reducing employee costs by up to 90%."
		},
		{
			title: "A monthly $300 wellness budget",
			description: "Use it on what your team needs most: VO2 tests, dental, vision, sleep tech, and more. Unused funds carry over, up to $3,300 per year."
		},
		{
			title: "Care you can actually trust",
			description: "We work with vetted providers and link records across visits so your team can finally see the full picture of their health in one place."
		}
	]}
/>

<UseCases
	title="Use Cases"
	subtitle="Real-world ways your team benefits"
	useCases={[
		{
			title: "Longevity planning for every employee",
			description: "DNA health tests and quarterly blood panels give your team personalized health insights—so they stay healthy and feel valued year-round.",
			image: "/generated/image-a-young-startup-employee-with-a-look-of-.webp",
			link: {
				href: "/use-cases/longevity-health-benefits",
				label: "Learn more"
			}
		},
		{
			title: "Accident support with real cost advocacy",
			description: "If an accident happens, we handle the bills, negotiate costs, and pay the provider—so your team stays focused on recovery, not paperwork.",
			image: "/generated/image-in-a-modern-and-vibrant-office-setting-a.webp",
			link: {
				href: "/use-cases/accident-cost-advocacy",
				label: "Learn more"
			}
		},
		{
			title: "Flexible wellness budget, real results",
			description: "From wearable sleep trackers to therapy sessions, every employee gets $300 monthly for the health tools and care they value most.",
			image: "/generated/image-a-startup-employee-is-in-a-bright-and-op.webp",
			link: {
				href: "/use-cases/flexible-health-budget",
				label: "Learn more"
			}
		}
	]}
/>

<AboutTeaser />
<CallToAction
  title="Tired of health benefits that just don't work?"
  subtitle="Smarter benefits, with no surprise bills or support gaps."
  description="Rivendell gives your team unlimited primary care, zero-deductible coverage, and a $300 flexible budget—starting today. No paperwork headaches, no out-of-network hassles, just better health care for your startup."
  imageSrc="/generated/image-a-cheerful-startup-team-member-beaming-w.webp"
  callsToAction={[
    {
      label: 'Start your plan today',
      href: '/get-started',
      variant: 'primary',
    },
    {
      label: 'Talk to our team',
      href: '/contact-sales',
      variant: 'secondary',
    },
  ]}
/>
