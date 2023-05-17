<template>
	<Nav />
	<div class="pt-24 md:px-20 px-5">
		<div>
			<p class="font-semibold font-serif" style="font-size: 25px;">{{post.title}}</p>
		</div>
		<div class="flex justify-center pt-10 flex-wrap">
			<div class="w-full p-5">
				<div class="p-4 border">
					<p class="text-gray-700">{{post.desc}}</p>
					<br />
					<NuxtLink to="/posts" class="text-emerald-500 underline">Kembali</NuxtLink>
				</div>
			</div>
		</div>
	</div>
</template>

<script setup>
	const route = useRoute()
	const id = route.params.id

	let post = []
	function getPost(id) {
		const posts = [
					{id: 1, title: "Apa itu HTML", desc: "HTML adalah bahasa markup."},
					{id: 2, title: "Apa itu CSS", desc: "CSS berguna untuk menghias tampilan website."},
					{id: 3, title: "Apa itu PHP", desc: "PHP singkatan dari PHP Hypertext Preprocessor."},
				]
		return posts.find(post => post.id == id)
	}
	post = getPost(id)
</script>
