<script>
  export let text;
  export let ariaLabel;
  export let link;
  import style from 'svelte-inline-style'


    let styles = {
      fontSize:'1rem',
      border: '1px solid var(--ashley-white)',
      color:'var(--ashley-white)',
      display: 'block',
      width: '100%',
      textTransform: 'lowercase',
      cursor: 'pointer',
      textAlign: 'center',
      textDecoration: 'none'
    }
</script>

<style>
.padding {
  padding-block: .8rem;
}

.sleepbutton {
  max-width: 100%;
  background: transparent
}

.sleepbutton:hover {
  background: rgba( 250,250,250, .1)
}

@media (min-width: 480px) {
  .sleepbutton {
    max-width: 13rem
  }
}
</style>

<a href={link} :aria-label={ariaLabel} class="padding sleepbutton"  use:style={styles}>
    {text}
</a>