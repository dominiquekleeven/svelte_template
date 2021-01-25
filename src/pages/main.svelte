<script lang="ts">
  import { onMount } from "svelte";
  import Component_template from "../components/component_template.svelte";
  import type TemplateModel from '../models/TemplateModel';


  let test : TemplateModel = {
    name: "Svelte"
  }

  onMount(async () => {
    document.title = "Hello World";
  });

  // process.env.API_URL    - access environment variables
</script>

<div class="content">
  <h1>Hello {test.name}</h1>

  <Component_template />
</div>

<style type="text/scss">
</style>
