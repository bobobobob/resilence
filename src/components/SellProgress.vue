<template>
  <div class="row">
      <div v-for="(f, i) in fragments" :key="i">
        <q-linear-progress >
        </q-linear-progress>
      </div>

  </div>
</template>

<script>
export default {
  props: {
    count: {
      type: Number,
      deault: 5007
    }
  },
  data () {
    return {
      fragments: [[1000, 5], [3000, 10], [3000, 15], [3000, 25], [1000, 50], [1000, 200], [1000, 500]]
    }
  },
  computed: {
    sold () {
      const res = []
      let total = 0
      const sold = this.count
      this.fragments.array.forEach(element => {
        const s = total
        const e = s + element[0]
        const stop = Math.min(sold, e)
        res.push({
          start: s,
          end: e,
          stop,
          price: element[1]
        })
        total = stop
      })
      return res
    }
  }
}
</script>

<style>

</style>
