<script setup lang="ts">
import Background from "../components/Home/Background.vue";
import Title from "~/components/Home/Title.vue";
import Content from "~/components/Home/Content.vue";
</script>

<template>
	<div class="mx-auto h-screen w-screen overflow-hidden rounded-md">
		<Background
			background-color="zinc-900"
			class="flex size-full flex-col items-center justify-center px-2 py-4 md:px-10"
		>
			<Title />

			<!--
			<div class="hidden lg:block h-96"></div>

			<InteractiveHoverButton class="hidden lg:block mt-64 absolute border-zinc-800">
				Discover API
			</InteractiveHoverButton>
			-->

			<Content />
		</Background>
	</div>
</template>
