<script>
  import { onMount } from "svelte";
  import Component_template from "../components/component_template.svelte"

  onMount(async () => {
    document.title = "Hello World"
  });

  // process.env.API_URL    - access environment variables
</script>

<style type="text/scss">
</style>

<div class="content">
  <h1>Hello Svelte</h1>
  
  <Component_template></Component_template>
</div >