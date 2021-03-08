<template>
  <q-layout>    
      <Select />
      <br>
      <div class="row q-col-gutter-x-xs q-col-gutter-y-lg q-pa-lg">
        <div class="col-md-2 col-6" v-for="(item, index) in destinationFilter" v-bind:key="index">
            <Card :data="item"/>
        </div>
      </div>    
  </q-layout>
</template>

<script>

import Header from '../components/Header'
import Select from '../components/Select.vue'
import Card from '../components/Card.vue'

import { mapActions, mapState } from 'vuex'


export default {
  name: 'PageIndex',
  components: {
    Header,
    Select,
    Card
  },
  data () {
    return {
      model: ''
    }
  },
  computed: {
    ...mapState(['ports', 'destination', 'routeJsonPorts', 'routeJsonDestinations', 'destinationFilter'])
  },
  methods: {
    ...mapActions(['actionSetsData', 'filterData'])
  },
  mounted () {
    this.actionSetsData({ route: this.routeJsonPorts, mutation: 'setPorts', ports: true })
    this.actionSetsData({ route: this.routeJsonDestinations, mutation: 'setDestinations', ports: false })
  }
}
</script>
