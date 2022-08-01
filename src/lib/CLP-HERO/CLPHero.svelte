<script>
  import Title from './heroTitle.svelte'
  import Button from '../Button.svelte'
  import BodyText from '../BodyText.svelte'
  import Container from '../Structure/Container.svelte'
  import style from 'svelte-inline-style'

  export let content

  let logo = "https://ik.imagekit.io/cpds/SleepCLP_TEST/ASHLEYSLEEP_5-yZD99Dc.svg?ik-sdk-version=javascript-1.4.3&updatedAt=1658402662259"

  let styles = {
    fontSize:'1rem',
    background:'var(--ashley-black)',
  }
  
</script>

<style>
.hero{
  position: relative;
  margin-inline: auto;
  max-height: auto;
  max-width: 1440px;
  overflow: hidden;

}

.content {
  padding: 2rem;
  text-align: center;
  display: flex;
  flex-direction: column;
  gap: 1rem;
  position: relative;
  flex:1;
  height:100%;
  box-sizing: border-box;
  align-items: center;
  justify-content: center;
}

/* .spacer {
  display: flex;
  flex-direction: column;
  gap: 1rem;
} */

.img { 
  display: block;
  block-size: auto;
 width:100%
}

@media (min-width: 480px) {
  
  
}

@media (min-width: 768px) {
  .img {
     height: 450px;
     object-fit: cover;
    object-position:right;
  }
  .content {
    max-width: 340px;
    position: absolute;
    text-align: start;
    align-items: start
  }
}
@media (min-width: 1024px) {
  .hero{

}
  
}
</style>

<div class="hero">

  <Container class="clp-container  [ flex ]">
    <div use:style={styles} class="content [ hotspot-image hotspot-v2-container ] ">
      <div>
          <img src={logo} alt="" height="20">
          <Title text={content.title} />
      </div>
      <BodyText light={true} text={content.text}/>
      <Button ariaLabel={content.ariaLabel} link={content.link} text={"Shop all"}/>
    </div>
  </Container>
  <picture>
    <source srcset={content.desktopImg} media="(min-width: 1024px)">
    <source srcset={content.tabletImg} media="(min-width: 480px)">
    <img class="img" src={content.mobileImg} alt={content.altText}/>
  </picture>
</div>