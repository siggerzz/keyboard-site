<template>
<div class="card">
  <div class="card-image">
    <figure class="image is-4by3">
      <img :src="creator.cardImage" alt="Creator Card Image">
    </figure>
  </div>
  <div class="card-content">
    <div class="media">
      <div class="media-left">
        <figure class="image is-48x48">
          <img :src="creator.logo" alt="Creator logo image">
        </figure>
      </div>
      <div class="media-content">
        <p class="title is-4">{{creator.name}}</p>
        <p class="subtitle is-4"><a :href="twitterUrl" class="subtitle is-6">@{{creator.twitterHandle}}</a></p>

    <div class="content">
      Lorem ipsum dolor sit amet, consectetur adipiscing elit.
      Phasellus nec iaculis mauris. <a>@bulmaio</a>.
      <a href="#">#css</a> <a href="#">#responsive</a>
      <br>
      <time datetime="2016-1-1">11:09 PM - 1 Jan 2016</time>
    </div>
        </div>
  </div>
</div>
  </div>
</template>

<script>
export default {
  props: {
    creator: {
      required: true
    }
  },
  data () {
    return {
      twitterUrl: `https://www.twitter.com/${this.creator.twitterHandle}`
    }
  }
}
</script>
