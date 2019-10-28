<script>
  /* this appears odd... I think we're effectively exporting a reference to var being used in the component which we're picking up in the parent */
  export let item;
  export let removeItem;
</script>

<style>
  li {
    list-style-type: none;
  }
  .done span {
    opacity: 0.5;
  }
</style>

<li class:done={item.done}>
  <input type="checkbox" bind:checked={item.done} />
  <span>{item.name}</span>
  <!-- event handlers use on:event syntax -->
  <button on:click={() => removeItem(item)}>❌</button>
</li>
