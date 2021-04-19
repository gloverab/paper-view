<script lang='ts'>
  export let name: string
  export let img: string
  export let link: string
</script>

<a href='https://www.facebook.com/events/786045325352442' class='recent-event'>
  <h4>{name}</h4>
  <img src={img} alt={name} />
</a>

<style>
  .recent-event {
    width: 600px;
    height: 600px;
    margin-right: 4rem;
  }

  h4 {
    color: yellow;
    padding: 0;
    margin: 0;
  }

  img {
    height: 100%;
    width: auto;
  }
</style>

