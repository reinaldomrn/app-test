<template>
    <q-select
        filled
        v-model="port"
        :options="ports"
        label="Destination"
        @input="filterData(port)"
    >
        <template v-slot:append>
        </template>
    </q-select>
</template>

<script>
import { mapState, mapActions } from 'vuex'
export default {
  name: 'Select',
  data () {
    return {
      port: ''
    }
  },
  computed: {
    ...mapState(['ports'])
  },
  methods: {
    ...mapActions(['filterData']),
    mmlo (a) {
      console.log(a)
    }
  },
  mounted () {

  }
}
</script>
