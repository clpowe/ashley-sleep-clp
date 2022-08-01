<script>
import style from 'svelte-inline-style'

    let styles = {
      fontSize:'1.75rem',
      lineHeight: '2.5rem',
      fontWeight: '900',
      textTransform: 'lowercase'
    }
</script>

<h2 use:style={styles}>
  <slot></slot>
</h2>