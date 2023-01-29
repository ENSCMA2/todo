<!-- #Component -->
<!-- components/FilterButton.svelte -->
<script lang='ts'>
  import { Filter } from '../types/filter.enum'

  export let filter: Filter = Filter.ALL
</script>

<div class="filters btn-group stack-exception">
  <button class="btn toggle-btn" class:btn__primary={filter === Filter.ALL} aria-pressed={filter === Filter.ALL} on:click={()=> filter = Filter.ALL} >
    <span class="visually-hidden">Show</span>
    <span>All</span>
    <span class="visually-hidden">tasks</span>
  </button>
  <button class="btn toggle-btn" class:btn__primary={filter === Filter.ACTIVE} aria-pressed={filter === Filter.ACTIVE} on:click={()=> filter = Filter.ACTIVE} >
    <span class="visually-hidden">Show</span>
    <span>Active</span>
    <span class="visually-hidden">tasks</span>
  </button>
  <button class="btn toggle-btn" class:btn__primary={filter === Filter.COMPLETED} aria-pressed={filter === Filter.COMPLETED} on:click={()=> filter = Filter.COMPLETED} >
    <span class="visually-hidden">Show</span>
    <span>Completed</span>
    <span class="visually-hidden">tasks</span>
  </button>
</div>

<style>

.btn.toggle-btn {
  color: #002211;
  border-color: #00ff22;
  border-width: 6px
}

.btn.toggle-btn.btn__primary {
  color: #ff2211;
  border-color: #00ff22;
  border-width: 10px
}



</style>