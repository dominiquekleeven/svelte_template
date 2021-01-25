<script>
  import { onMount } from "svelte";
  import Component_template from "../components/component_template.svelte";

  onMount(async () => {
    document.title = "Hello World";
  });

  // process.env.API_URL    - access environment variables
</script>

<div class="content">
  <h1>Hello Svelte</h1>

  <Component_template />
</div>

<style type="text/scss">
</style>
