<script>
import Button from './Button.svelte'
import BodyText from './BodyText.svelte'
import Section from './Section.svelte'
import Container from './Structure/Container.svelte'

export let ad

</script>

<style>
.holder {
  display: grid;
  grid-template-columns: 1fr;
  color: var(--ashley-white)
}

.img {
  overflow: hidden;
  height: 100%;
  
}

.img > img {
  height: 100%;
    object-fit: cover;
    max-inline-size: 100%;
}

.content {
  background: var(--ashley-deepblue);
  display: grid;
  place-content: center;
  text-align: center;
  justify-items: center;
  gap: 1.25rem;
  padding: 2rem 1rem
}

@media (min-width: 786px){

.holder {
  display: grid;
  grid-template-columns: 1fr 1fr;
  color: var(--ashley-white)
}

.content {
  background: var(--ashley-deepblue);
  display: grid;
  place-content: center;
  text-align: center;
  justify-items: center;
  
}
}
</style>

<Section>
  <Container>
    <div class="holder">
    <div class="img">
      <img src={ad.img} height="310px" alt={ad.ariaLabel}>
    </div>
      <div class="content [ hotspot-image hotspot-v2-container ]">
        <p>{ad.headline}</p>
        <img src={ad.logo} alt="">
        <BodyText light={true} small={true} text={ad.body} />
        <Button ariaLabel={ad.ariaLabel} link={ad.link} text={"learn more"}/>
      </div>
    </div>
  </Container>
</Section>