<script lang="ts">
  import Main from "./pages/Main.svelte";
  import Router from "page";
  import { onMount } from "svelte";

  let page : any;
  let params : any;

  onMount(async () => {
    setup_routes();
  });

  async function setup_routes() {
    Router("/", () => (page = Main));
    Router.start();
  }
</script>

<main>
  <svelte:component this={page} {params} />
</main>

<style type="text/scss">
  main {
    height: 100%;
    width: 100%;
    display: flex;
    justify-content: center;
  }
</style>
