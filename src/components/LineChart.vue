<script>
import { Line } from "vue-chartjs";

export default {
  extends: Line,
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
            data: [6.6, 7.7, 6.2, 1, 4, 7.1, 5.7, 1],
            backgroundColor: "transparent",
            borderColor: "rgba(1, 116, 188, 0.50)",
            pointBackgroundColor: "rgba(171, 71, 188, 1)"
          }
        ]
      },
      {
        responsive: true,
        maintainAspectRatio: false,
        title: {
          display: true,
          text: "My Data"
        }
      }
    );
  }
};
</script>