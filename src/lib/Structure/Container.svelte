<script>
</script>

<style>
.clp-container {
  inline-size: 100%;
  margin-inline: auto;
}

@media (min-width: 768px) {
  .clp-container {
    inline-size: min(100% - max(1rem, 5%), 1240px);
  }
}
</style>

<div class="clp-container">
<slot></slot>
</div>