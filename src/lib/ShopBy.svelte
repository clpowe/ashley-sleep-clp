<script>
  import Section from './Section.svelte'
  import Container from './Structure/Container.svelte'
  import FixedH4 from './FixedHeaderFour.svelte'
  import IconListItem from './IconIistItem.svelte'
  import style from 'svelte-inline-style'

    let link = {
      color:'unset',
      textDecoration: 'none'
    }

  export let catagories
  
</script>

<style>
.shopby {
  display: grid;
  grid-template-columns: 1fr;
}

.shopby > div {
 padding-block: 2rem;
 padding-inline: 1rem
}

.shopby > div:nth-child(even) {
   background-color: var(--gray-200)
}

ul {
  list-style-type: none;
  margin: 0;
  padding: 0;
}

.itemContainer {
  padding-block: 1.25rem;
}

.itemContainer:last-child{
  border-bottom: 1px solid var(--gray-300);
}


.link:hover {
  background-color: #f4f4f4
}

.holder {
  display: flex;
  flex-direction: column;
  gap: 1rem
}

@media (min-width: 768px)
{
  .shopby {
    grid-template-columns: repeat(1, 1fr);
  }

  .shopby > div:nth-child(even) {
   background-color: transparent
  }

}
@media (min-width: 1024px)
{
  .shopby {
    grid-template-columns: repeat(3, 1fr);
  }

}

</style>

<Section>
  <Container>
    <div class="shopby">
      {#each catagories as list}
        <div class="holder ">
          <FixedH4>
            {list.heading}
          </FixedH4>
          <ul class=" [ hotspot-image hotspot-v2-container ] ">
            {#each list.list as item}
              <a href={item.link} ariaLabel={item.ariaLabel} use:style={link} > 
                <li class="itemContainer link">
                    <IconListItem img={item.icon}>
                    {item.text}
                    </IconListItem>
                </li>
              </a>
            {/each}
          </ul>
        </div>
      {/each}
    </div>
  </Container>
</Section>