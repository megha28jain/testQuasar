<template>
  <q-page class="layout-breakpoint">
    <div class="text-grey row justify-end q-px-xl q-mx-xl" style="font-size: 3em">
          <q-icon name="photo" />
          <q-icon name="notifications" />
          <q-icon name="person" />
        </div>
    <div class="flex">
      <div class="content-area">
        <q-card flat class="my-card">
          <q-card-section>
            <faq-questions/>
          </q-card-section>
        </q-card>
      </div>
      <div class="my-width">
          <fundraising-block/>
          <investment-block/>
      </div>
    </div>
  </q-page>
</template>

<script>
import FundraisingBlock from '../components/FundraisingBlock.vue'
import InvestmentBlock from '../components/InvestmentBlock.vue'
import FaqQuestions from '../components/FaqQuestions.vue'

export default {
  name: 'PageIndex',
  components: {
    FundraisingBlock,
    InvestmentBlock,
    FaqQuestions
  }
}
</script>

<style lang="sass" scoped>
  @media only screen and (max-width: 1152px)
    .layout-breakpoint
      padding: .5rem
  .content-area
    text-overflow: ellipsis
    max-width: 50%
    overflow-wrap: break-word
  .my-width
    max-width: 40%
</style>
