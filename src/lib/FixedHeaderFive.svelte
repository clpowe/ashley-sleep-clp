<script>
import style from 'svelte-inline-style'

export let light = false

  let styles = {
    fontSize:'1.25rem',
    lineHeight: '1.75rem',
    fontWeight: '900',
  }
</script>

<style>
  .text-light {
    color: var(--ashley-white)
  }
  .text-dark {
    color: var(--ashley-black)
  }
</style>

<p use:style={styles} class={ light ? 'text-light' : 'text-dark' }>
  <slot></slot>
</p>