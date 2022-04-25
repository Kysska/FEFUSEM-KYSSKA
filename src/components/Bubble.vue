<template>
  <Bubble
    :chart-options="chartOptions"
    :chart-data="chartData"
    :chart-id="chartId"
    :dataset-id-key="datasetIdKey"
    :plugins="plugins"
    :css-classes="cssClasses"
    :styles="styles"
    :width="width"
    :height="height"
  />
</template>

<script>
import { Bubble } from 'vue-chartjs/legacy'

import {
  Chart as ChartJS,
  Title,
  Tooltip,
  Legend,
  PointElement,
  LinearScale
} from 'chart.js'

ChartJS.register(Title, Tooltip, Legend, PointElement, LinearScale)

export default {
  name: 'BubbleChart',
  components: {
    Bubble
  },
  props: {
    chartId: {
      type: String,
      default: 'bubble-chart'
    },
    datasetIdKey: {
      type: String,
      default: 'label'
    },
    width: {
      type: Number,
      default: 400
    },
    height: {
      type: Number,
      default: 400
    },
    cssClasses: {
      default: '',
      type: String
    },
    styles: {
      type: Object,
      default: () => {}
    },
    plugins: {
      type: Array,
      default: () => []
    }
  },
  data() {
    return {
      chartData: {
        datasets: [
          {
            label: 'Конструктивные копинги',
            backgroundColor: '#f87979',
            data: [
              {
                label: 'Планирование решения проблемы',
                x: 20,
                y: 25,
                r: 44
              },
              {
                  label: 'Самоконтроль',
                x: 40,
                y: 10,
                r: 66
              },
              {
                  label: 'Поиск социальной поддержки',
                x: 30,
                y: 22,
                r: 22
              }
            ]
          },
          {
            label: 'Неконструктивные копинги',
            backgroundColor: '#7C8CF8',
            data: [
              { 
                label: "Конфронтационный копинг",
                x: 10,
                y: 30,
                r: 33
              },
              {
                label: "Дистанцирование",
                x: 20,
                y: 20,
                r: 88
              },
              {
                label: "Бегство-избегание", 
                x: 15,
                y: 8,
                r: 75
              }
            ]
          },
          {
            label: 'Относительно конструктивные',
            backgroundColor: '#f87456',
            data: [
              {
                label: 'Принятие ответственности',
                x: 25,
                y: 15,
                r: 83
              },
              {
                  label: 'Положительная переоценка',
                x: 35,
                y: 20,
                r: 23
              }
            ]
          }
        ]
      },
      chartOptions: {
        responsive: true,
        maintainAspectRatio: false
      }
    }
  }
}
</script>
