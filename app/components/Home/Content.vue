<script setup lang="ts">
import Spotlight from "../Card/Spotlight.vue";

const cards = [
	{
		title: "Corpus",
		description: "Image recognition model to detect nudity.",
		url: "https://github.com/Gravitalia/remini/tree/master/corpus",
	},
	{
		title: "Superego",
		description: "Detects inappropriate written behavior.",
		url: "https://github.com/Gravitalia/remini/tree/master/superego",
	},
];
</script>

<template>
	<div class="mt-96 grid lg:grid-cols-2 2xl:grid-cols-3 gap-6 p-6">
		<Spotlight
			v-for="card in cards"
			:key="card.title"
			class="shadow-2xl bg-zinc-900 border-zinc-800 text-white p-4 max-w-xl"
			gradient-color="#8b5cf650"
		>
			<h3 class="flex text-md lg:text-lg">
				{{ card.title }}
				<NuxtLink
					v-if="card.url"
					tabindex="0"
					:to="card.url"
					class="cursor-pointer"
				>
					<svg
						xmlns="http://www.w3.org/2000/svg"
						width="17"
						viewBox="0 0 17 17"
						class="mt-1.5 ml-2 fill-zinc-400 hover:fill-white"
					>
						<g clip-path="url(#a)">
							<path
								fill="currentColor"
								fill-rule="evenodd"
								d="M8.977.83C4.549.83.97 4.32.97 8.636c0 3.45 2.293 6.371 5.475 7.405.397.078.543-.168.543-.375 0-.18-.013-.8-.013-1.447-2.227.465-2.691-.93-2.691-.93-.358-.905-.888-1.138-.888-1.138-.73-.478.053-.478.053-.478.808.052 1.233.801 1.233.801.715 1.19 1.869.853 2.333.646.066-.504.278-.853.504-1.046-1.777-.181-3.646-.853-3.646-3.852 0-.853.318-1.55.822-2.093-.08-.194-.358-.995.08-2.068 0 0 .676-.207 2.2.801a7.94 7.94 0 0 1 2.002-.258c.676 0 1.365.09 2.001.258 1.525-1.008 2.2-.801 2.2-.801.438 1.073.16 1.874.08 2.068.517.542.822 1.24.822 2.093 0 2.999-1.869 3.658-3.659 3.852.292.245.544.71.544 1.447 0 1.047-.013 1.887-.013 2.145 0 .207.146.453.543.375 3.182-1.034 5.475-3.955 5.475-7.405C16.983 4.319 13.39.83 8.977.83Z"
								clip-rule="evenodd"
							/>
						</g>
					</svg>
					<span class="sr-only">GitHub</span>
				</NuxtLink>
			</h3>
			<p class="text-xs lg:text-sm">
				{{ card.description }}
			</p>
		</Spotlight>
	</div>
</template>
