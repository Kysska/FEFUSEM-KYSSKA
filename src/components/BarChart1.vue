<script>
import { Bar } from "vue-chartjs";

export default {
  extends: Bar,
  mounted() {
    this.renderChart(
      {
        labels: [
        "Техника",
          "Наука",
          "Искусство",
          "Общение",
          "Бизнес",
          "Знак",
          "Природа",
          "Риск"
        ],
        datasets: [
          {
            label: "Интересы",
            backgroundColor: "#f87979",
            data: [6.6, 7.7, 6.2, 1, 4, 7.1, 5.7, 1]
          }
        ]
      },
      { responsive: true, maintainAspectRatio: false }
    );
  }
};
</script>
