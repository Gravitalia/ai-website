<script setup lang="ts">
import Spotlight from "~/components/Card/Spotlight.vue";
import Background from "../components/Home/Background.vue";
</script>

<template>
	<div class="mx-auto h-screen w-screen overflow-hidden rounded-md">
		<Background
			background-color="zinc-900"
			class="flex size-full flex-col items-center justify-center px-2 py-4 md:px-10"
		>
			<div class="absolute">
				<h1 class="text-center text-white text-6xl">Gravitalia AI</h1>
				<h2
					class="mt-6 px-4 text-center text-xl text-zinc-400 md:text-2xl font-thin"
				>
					Machine learning models made for embedded systems.
				</h2>
			</div>

			<!--
			<div class="hidden lg:block h-96"></div>

			<InteractiveHoverButton class="hidden lg:block mt-64 absolute border-zinc-800">
				Discover API
			</InteractiveHoverButton>
			-->

			<div class="mt-96 grid lg:grid-cols-2 2xl:grid-cols-3 gap-6 p-6">
				<Spotlight
					class="cursor-pointer shadow-2xl bg-zinc-900 border-zinc-800 text-white p-4 max-w-xl"
					gradient-color="#8b5cf650"
				>
					<h3 class="text-md lg:text-lg">Corpus</h3>
					<p class="text-xs lg:text-sm">
						Image recognition model to detect nudity.
					</p>
				</Spotlight>
				<Spotlight
					class="cursor-pointer shadow-2xl bg-zinc-900 border-zinc-800 text-white p-4 max-w-xl"
					gradient-color="#8b5cf650"
				>
					<h3 class="text-md lg:text-lg">Superego</h3>
					<p class="text-xs lg:text-sm">
						Detects inappropriate written behavior.
					</p>
				</Spotlight>
			</div>
		</Background>
	</div>
</template>
