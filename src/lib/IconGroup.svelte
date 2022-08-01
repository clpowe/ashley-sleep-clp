<script>
import Fixed5 from './FixedHeaderFive.svelte'
import BodyText from './BodyText.svelte'

export let ig

let link = true

</script>

<style>
.holder {
  display: grid;
  grid-template-columns: 5rem auto;
  grid-template-rows: auto;
  gap: 1.25rem;
  padding-inline: 1rem;
  flex: 1 1 0px;
  text-align: start
}
.img {
  justify-self: center;
}

.img > img {
  max-inline-size: 100%;
  block-size: auto;
}

@media (min-width: 768px){
  .holder {
    grid-template-columns: auto;
    grid-template-rows: 64px auto;
    text-align: center
  }
}
</style>

<div class="holder">
  <div class="img">
    <img src={ig.icon} alt="">
  </div>
  <div class=" [ hotspot-image hotspot-v2-container ] ">
    <div>
      <Fixed5>
        {ig.title}
      </Fixed5>
    </div>
    <BodyText light={false} small={true} text={ig.text} />
    {#if ig.link}
      <a href={ig.link} :aria-label={ig.ariaLabel}>
       learn more
      </a>
    {/if}
  </div>
</div>