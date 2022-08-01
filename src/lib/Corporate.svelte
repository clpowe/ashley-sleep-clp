<script>
import Section from './Section.svelte'
import Container from './Structure/Container.svelte'
import FixedH4 from './FixedHeaderFour.svelte'
import IconGroup from './IconGroup.svelte'

export let corporate

</script>

<style>
.center {
  text-align: center;
  padding-inline: 1rem;
  margin-bottom: 3rem;
}

.list {
  display: flex;
  flex-direction: column;
  gap: 2.5rem
}
.list:not(:last-child) {
    background: red
  }

@media (min-width: 768px){
  .list {
    flex-direction: row;
    justify-content: space-between;
    gap: 1rem
  }

  
}
</style>

<Section>
  <Container>
    <div class="center">
      <FixedH4>
        we’re joining the sleep revolution
      </FixedH4>
    </div>
    <div class="list [ hotspot-image hotspot-v2-container ]">
      {#each corporate as ig}
        <IconGroup ig={ig}/>
      {/each}
    </div>
  </Container>
</Section>