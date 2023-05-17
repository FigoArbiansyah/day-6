<template>
	<nav class="flex justify-between items-center py-5 px-14 bg-white text-black fixed top-0 w-full">
		<div>
			<h3 class="text-xl font-semibold font-serif">
				<NuxtLink to="/">My Posts</NuxtLink>
			</h3>
		</div>
		<div>
			<ul class="flex gap-x-4">
				<li>
					<NuxtLink to="/about" class="text-lg hover:font-semibold">About</NuxtLink>
				</li>
				<li>
					<NuxtLink to="/posts" class="text-lg hover:font-semibold">Posts</NuxtLink>
				</li>
			</ul>
		</div>
	</nav>
</template>