<script>
export let img
</script>

<style>
.holder{
  display: grid;
  grid-template-columns: 2rem auto;
  align-items: center;
  gap: 2rem;
  min-height: 32px
}
.text{
  font-size: 1rem;
  text-transform: uppercase;
  letter-spacing: .1rem;
}

.icon{
  place-self: center
}
</style>

<div class="holder">
  <img class="icon" src={img} alt=""/>
  <p class="text">
    <slot>
    </slot>
  </p>
</div>