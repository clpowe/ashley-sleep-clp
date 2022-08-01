<script>
  import style from 'svelte-inline-style'

  export let text;

</script>

<style>
  .text{
    color: var(--ashley-white);
    font-weight: 700;
    font-size: 1.5rem
  }

  @media (min-width: 480px) {
    .text {
      
    }
	}
</style>

<h1 class="text">{text}</h1>