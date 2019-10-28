<script>
  import TodoItem from "./TodoItem.svelte";

  let items = [
    { id: 1, name: "make cofffffe", done: true },
    { id: 2, name: "build speakers", done: false },
    { id: 3, name: "????", done: false },
    { id: 4, name: "profit", done: false }
  ];

  let title;
  let name;

  const addItem = () => {
    items = [
      ...items,
      {
        id: Math.random(),
        name,
        done: false
      }
    ];

    name = "";
  };

  const removeItem = item => {
    /* 
			For svelte to recompute/re-render the variable needs to be reassigned.

			It also notices assignments to properties: items[0] = "something"
		*/
    items = items.filter(i => i != item);
  };
</script>

<style>
  h1 {
    color: purple;
  }
</style>

<h1>Todos 🗒</h1>

<form on:submit|preventDefault={addItem}>
  <label for="title">
    Add item:
    <input id="title" type="text" bind:value={name} />
  </label>
</form>

<ul>
  {#each items as item}
    <!-- shorthand for attributes/props... instead of item={item} -->
    <TodoItem {item} {removeItem} />
  {/each}
</ul>
