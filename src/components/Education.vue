<template>
  <div>
    <v-timeline>
      <v-timeline-item
        v-for="(value, i) in payloads"
        :key="i"
        :color="value.color"
        small
      >
        <template v-slot:opposite>
          <span
            :class="`subtitle-1 font-weight-bold ${value.color}--text`"
            v-text="value.year"
          ></span>
        </template>
        <div class="pb-4 pt-5">
          <h2 :class="`subtitle-2 font-weight-light pb-4 ${value.color}--text`">
            {{value.text}}
          </h2>
        </div>
      </v-timeline-item>
    </v-timeline>
  </div>
</template>
<script>
export default {
  data(){
    return {
      payloads: [
        {
          color: 'pink',
          year: '2006 - 2012',
          text: 'SDN JATI 4 TANGERANG'
        },
        {
          color: 'cyan',
          year: '2012 - 2015',
          text: 'SMPN 08 TANGERANG'
        },
        {
          color: 'grey',
          year: '2015 - 2018',
          text: 'SMK PANCAKARYA ~ MULTIMEDIA'
        },
      ],
    }
  }
}
</script>