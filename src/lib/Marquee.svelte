<script>
import Section from './Section.svelte'
import Container from './Structure/Container.svelte'
import Button from './Button.svelte'
import Fixed5 from './FixedHeaderFive.svelte'
import IconListItem from './IconIistItem.svelte'

export let marquees

</script>

<style>
.flow {
  display: flex;
  flex-direction: column;
  gap: 5rem
}

.marquee {
  width: 100%;
  display: grid;
  grid-template-columns: auto;
}

.marquee > .img {
  display: none;
  overflow: hidden
}

 .img > picture {
    height: 100%;
    width: 100%;
    object-fit: cover;
    max-inline-size: 100%;
    object-position: center;
} 

.mainImg {
    height: 100%;
    object-fit: cover;
    max-inline-size: 100%;
    object-position: 20%;
}

.info {
  display: grid;
  place-content: center;
  justify-items: center;
  background: var(--ashley-black);
  padding-inline: 2rem;
  padding-block: 1rem;
  text-align: center;
  min-height: 360px;
  gap: 2rem;
}

.info > img {
  max-inline-size: 100%;
  block-size: auto;
  max-width: 13rem;
}

.essentials {
  background: var(--ashley-essential)
}
.gruve {
  background: #B2E5F6
}
.align {
  background: #C3D9D5
}

ul {
  display: flex;
  flex-direction: column;
  gap: .875rem; 
  margin: 0;
  padding-block: 1rem;
  padding-inline: 2rem;
  list-style-type: none;
}

@media (min-width: 768px){
  .marquee {
    grid-template-columns: auto 416px;
  }

  .marquee > .img {
    display: block;
    height: 100%;
    overflow: hidden
  }

  .content {
    order: 1;
  }

  .marquee:nth-child(2) {
    grid-template-columns: 416px auto;
}

  .marquee:nth-child(2) > .img {
      order: 2
  }
}
</style>

<Section>
  <Container>
    <div class="flow">
      {#each marquees as marquee}
        <div class="marquee">
          <div class="img">
            <picture>
              <source srcset={marquee.mainImg} media="(min-width: 960px)" height="504" loading="eager" >
              <img class="mainImg" src={marquee.mobileImg} alt={marquee.altText} height="504"  loading="eager">
            </picture>
          </div>
          <div class="content">
            <div class="info [ hotspot-image hotspot-v2-container ]">
              <img src={marquee.logo} alt="" heaight="56">
              <Fixed5 light={true} >
                { marquee.mainText }
              </Fixed5>
              <Button ariaLabel={marquee.ariaLabel} link={marquee.link} text={"Shop now"}/>
            </div>
            <div class="align" class:essentials={marquee.variant==='essentials'} class:gruve={marquee.variant==='gruve'} class:align={marquee.variant==='align'}> 
              <ul>
              {#each marquee.list as list}
                <li class="">
                    <IconListItem img={list.icon}>
                      {list.text}
                    </IconListItem>
                </li>
              {/each}
              </ul>
            </div>
          </div>
        </div>
      {/each}
    </div>
  </Container>
</Section>