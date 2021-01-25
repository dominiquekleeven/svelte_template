<script lang="ts">
  import { onMount } from "svelte";
  import TestComponent from "../components/TestComponent.svelte";
  import type TemplateModel from "../models/TemplateModel";
  import { greeting } from '../modules/TestModule.svelte'

  let test: TemplateModel = {
    name: "Svelte",
  };

  export let params : any;

  onMount(async () => {
    document.title = "Hello World";
    greeting();
  });

  // process.env.API_URL    - access environment variables
</script>

<div class="content">
  <h1>Hello {test.name}</h1>
  <TestComponent />
</div>

<style type="text/scss">
</style>
