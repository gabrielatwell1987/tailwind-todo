<script>
    import {deleteTodo, toggleTodo, editTodo} from '../store/TodoStore';
    import DeleteIcon from './DeleteIcon.svelte';

    export let todo;

    $: completeClass = todo.complete ? 'complete' : 'in-progress';
</script>

<div class="flex items-center justify-between border-2 border-gray-200 px-5 py-4">
    <div class="flex w-full max-w-lg items-center justify-start">
        <label for={`${todo.id}-checkbox`} class="sr-only">Complete Todo</label>
        <input type="checkbox" id={`${todo.id}-checkbox`} checked={todo.complete} on:change={() => toggleTodo(todo.id)} class="h-4 w-4 border-gray-400 bg-slate-400 text-green-300 focus:border-green-500 focus:outline focus:outline-2 focus:outline-offset-2 focus:outline-green-500">

        <label for={`${todo.id}-text`} class="sr-only">Edit Todo</label>
        <input type="text" id={`${todo.id}-text`} value={todo.text} placeholder="Enter a Task..." on:input={(e) => editTodo(todo.id, e.target.value)} class="ml-5 flex-1 text-ellipsis rounded-none border-x-0 border-t-0 border-b border-dashed border-gray-300 bg-slate-300 px-0 pb-1 text-base font-normal text-gray-600 placeholder:text-gray-400 focus:border-gray-400 focus:outline-none focus:ring-0">

        <span class="{completeClass} ml-12 mr-12 hidden rounded-ful py-0.5 px-2 text-sm font-normal text-gray-400 md:block">{todo.complete ? 'Complete' : 'In Progress'}</span>

        <button type="button" on:click={() => deleteTodo(todo.id)} class="group ml-4 flex items-center justify-center rounded-md bg-gray-300 p-2 hover:bg-slate-500 focus outline-none focus-visible:outline-2 focus-visible:outline-offset-2 focus-visible:outline-green-800"><span class="sr-only">Delete Todo</span><DeleteIcon /></button>
    </div>
</div>

<style>

</style>