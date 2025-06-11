<!--

@component CustomerCardHero

This hero displays a row of customers. If used, we don't need a testimonial section on the same page.

It should ALWAYS have between 3 and 5 customers!
-->

<script lang="ts">
	// Components
	import AnimateText from "$lib/components/animation/AnimateText.svelte";
	import Button from "$lib/components/ui/Button.svelte";

	// Constants
	import { cta } from "$lib/navigation";
	import { onMount } from "svelte";
	import StakeholderCard from "../sub/StakeholderCard.svelte";
	import { animate, stagger } from "motion";
	import { page } from "$app/state";

	let cards: HTMLElement[] = $state([]);

	// Types
	type Props = {
		centered?: boolean;
		title: string;
		subtitle: string;
		customers: Array<{
			name: string;
			position?: string;
			imageSrc: string;
		}>;
		callsToAction?: Array<{
			href: string;
			label: string;
		}>; // A maximum of two calls to action, with the first one being primary and the second one being secondary
	};

	let {
		title,
		subtitle,
		customers = [],
		callsToAction = [cta],
		centered = false,
		...rest
	}: Props = $props();

	onMount(() => {
		if (window.self !== window.top) return;
		animate(
			cards,
			{
				// y: ["50%", 0],
				scale: [0.9, 1],
				filter: ["blur(4px)", "blur(0px)"],
				opacity: [0, 1]
			},
			{
				duration: 0.5,
				ease: "easeOut",
				delay: stagger(0.1, {
					startDelay: 0.5,
					ease: "easeInOut"
				})
			}
		);
	});
</script>

<div class="bg-background" {...rest}>
  <header
    class={[
      "section-px section-pt section-py container mx-auto grid items-end gap-16 gap-y-9 text-balance",
      centered ? "place-items-center text-center" : "xl:grid-cols-[1fr_auto]"
    ]}
    data-enter-container
  >
    <div class="grid max-w-prose gap-7 section-mb-sm">
      <h1 class="text-display w-full text-balance" data-enter>
        <span class="block"><AnimateText text={title} /></span>
      </h1>

      <p
        data-enter
        class={[
          "text-muted-foreground text-headline font-[425] block max-w-[45ch] text-pretty transition duration-500 ease-out opacity-90 section-mt-sm",
          centered && "mx-auto"
        ]}
      >
        {subtitle}
      </p>
    </div>
    {#if callsToAction.length > 0}
      <div class="flex flex-wrap gap-6 md:gap-8 section-mt-sm max-w-xl w-full justify-center md:justify-start" data-enter>
        {#each callsToAction as cta, index}
          <Button
            href={cta.href}
            size="lg"
            variant={index % 2 === 0 ? "primary" : "secondary"}
            class="max-lg:hidden cursor-pointer"
            >{cta.label}</Button
          >
          <Button
            href={cta.href}
            size="md"
            variant={index % 2 === 0 ? "primary" : "secondary"}
            class="lg:hidden cursor-pointer"
            >{cta.label}</Button
          >
        {/each}
      </div>
    {/if}
  </header>

  <div
    class="section-mt-sm border-t border-solid"
    style="border-color: var(--color-border);"
  >
    <div
      class="mt-6 grid flex-nowrap gap-(--card-gap) overflow-x-auto px-(--card-gap) whitespace-nowrap [--card-gap:calc(var(--radius)/2)] [--gap:--spacing(5)] max-lg:auto-cols-max max-lg:grid-flow-col md:whitespace-normal lg:grid-cols-[var(--cols)] lg:flex-wrap"
      style:--cols="repeat({customers.length},1fr)"
    >
      {#each customers as customer, index}
        <div class="h-full overflow-clip rounded-lg">
          <StakeholderCard bind:cards {...customer} {index} />
        </div>
      {/each}
    </div>
  </div>
</div>
