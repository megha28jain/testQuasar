<template>
  <div class="q-pa-md q-gutter-md">
    <q-card flat bordered class="my-card">
      <q-card-section>
        <q-item-label header class="text-h6">Fundraising progress</q-item-label>
        <div class="flex justify-between">
          <div class="flex-column example-cell">
            <div>Commited</div>
            <div>$650,000</div>
          </div>
          <div class="flex-column example-cell">
            <div>Minimum Goal</div>
            <div>$2,000,000</div>
          </div>
        </div>
        <div class="q-pa-md">
          <q-linear-progress size="10px" :value="progress" />
        </div>
        <div>32 investors in process<br />Closes by 30 Nov 2020</div>
      </q-card-section>
    </q-card>
  </div>
</template>
<script>
export default {
  data () {
    return {
      progress: 0.4
    }
  }
}
</script>
<style lang="sass" scoped>
.example-cell
    margin: 1px
    padding: 4px 8px
    box-shadow: inset 0 0 0 2px $grey-6
</style>
