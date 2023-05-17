<template>
	<Nav />
	<div class="pt-24 md:px-20 px-5">
		<div>
			<p class="font-semibold font-serif" style="font-size: 25px;">Postingan Blogo</p>
		</div>
		<div class="flex justify-center pt-10 flex-wrap">
			<div v-for="post in posts" :key="post.id" class="md:w-1/3 w-full p-5">
				<div class="p-4 border">
					<p class="text-xl font-semibold">{{post.title}}</p>
					<br />
					<NuxtLink :to="`/posts/${post.id}`" class="text-emerald-500 underline">Lihat</NuxtLink>
				</div>
			</div>
		</div>
	</div>
</template>

<script>
	export default {
		data () {
			return {
				posts: [
					{id: 1, title: "Apa itu HTML", desc: "HTML adalah bahasa markup."},
					{id: 2, title: "Apa itu CSS", desc: "CSS berguna untuk menghias tampilan website."},
					{id: 3, title: "Apa itu PHP", desc: "PHP singkatan dari PHP Hypertext Preprocessor."},
				]
			}
		}
	}
</script>
