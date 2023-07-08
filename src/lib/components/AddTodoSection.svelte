<script>
    import {addTodo} from '../store/TodoStore';
    import AddIcon from './AddIcon.svelte';
    import DeleteIcon from './DeleteIcon.svelte';
    import CheckIcon from './CheckIcon.svelte';
</script>

<section class="flex justify-between">
    <h3 class="text-xl font-bold text-gray-800">Checklist</h3>
    <button type="button" on:click={addTodo} class="group flex items-center rounded-md border-gray-200 bg-green-100 px-6 py-3 text-black text-lg font-semibold outline outline-2 outline-offset-2 outline-green-200 hover:bg-green-300 focus-visible:text-green-400 focus-visible:outline-green-300">Add Task<AddIcon/></button>
</section>