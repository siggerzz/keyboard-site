<template>
<section class="section">
  <div class="columns">
  <div class="column" v-for="creator in creators" :key="creator.name">
    <div>
    <CardComponent :creator='creator'/>
    </div>
    </div>
</div>
</section>
</template>

<script>

import CardComponent from '../components/CreatorCard'
// eslint-disable-next-line no-unused-vars
import CreatorsJson from '../data/creators.json'

export default {
  name: 'CreatorsPage',
  components: {
    CardComponent
  },
  data () {
    return {
      creators: CreatorsJson.creators
    }
  }
}
</script>
