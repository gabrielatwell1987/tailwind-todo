<script>
	import AddTodoSection from '$lib/components/AddTodoSection.svelte';
	import TodoSection from '$lib/components/TodoSection.svelte';
	import ProgressSection from '$lib/components/ProgressSection.svelte';
</script>

<div class="min-h-screen bg-amber-100 p-0 selection:bg-green-200 md:py-24 md:px-8 text-black">
	<main class="mx-auto min-h-screen max-w-none rounded-none bg-slate-200 px-5 py-10 outline-none md:min-h-max md:max-w-[60rem] md:rounded-2xl md:px-8 md:outline md:outline-4 md:outline-offset-8 md:outline-orange-100">
		<h1 class="text-2xl font-bold text-gray-700">Dashboard</h1>
		<div class="mt-10">
			<AddTodoSection />
			<TodoSection />
			<ProgressSection />
		</div>
	</main>
</div>