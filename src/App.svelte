<!-- #Component -->
<!-- App.svelte -->
<script lang="ts">
  <!-- #Component - same as Todos and Alert, this is where they are applied -->
  import Todos from './components/Todos.svelte'
  import Alert from './components/Alert.svelte'

  import { todos } from './stores'
</script>

<Alert />
<Todos bind:todos={$todos} />
