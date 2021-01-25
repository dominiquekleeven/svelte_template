<script>
  import Main from "./pages/main.svelte";
  import Router, { redirect } from "page";
  import { onMount, afterUpdate } from "svelte";

  let page;
  let params;

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
