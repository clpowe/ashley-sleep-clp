<script>
export let text
export let light = false
export let small = false

import style from 'svelte-inline-style'

  let styles = {
    
    
  }
</script>

<style>
  p {
    font-size: 1rem;
    line-height: 1.75rem;
    font-weight: 100;
    max-width: 55ch
  }

  .text-light {
    color: var(--ashley-white)
  }
  .text-dark {
    color: var(--ashley-black)
  }

  .small {
    font-size: 14px;
  }

  @media (min-width: 786px){
    .small {
    font-size: 1rem;
  }
  }
</style>

<p  class={ light ? 'text-light' : 'text-dark' }  class:small={small}> 
  {text}
</p>