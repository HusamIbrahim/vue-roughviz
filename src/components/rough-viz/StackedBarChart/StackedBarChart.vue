<template>
  <div ref="chartdiv"></div>
</template>

<script lang="ts">
import { defineComponent } from '@vue/composition-api'
import { StackedBar } from 'rough-viz'
import { stackedBarChartOptions } from '@/shared'
import { useSetupRoughVizChart } from '@/composables/rough-viz'

export default defineComponent({
  props: {
    ...stackedBarChartOptions,
  },
  setup(props) {
    const chartdiv = useSetupRoughVizChart(StackedBar, props)

    return { chartdiv }
  },
})
</script>
