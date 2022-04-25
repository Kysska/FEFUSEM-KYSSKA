<script>
import { Line } from "vue-chartjs";

export default {
  extends: Line,
  mounted() {
    this.renderChart(
      {
        labels: [
           "Активная, деятельная жизнь",
          "Здоровье",
          "Интересная работа",
          "Красота природы и искусства",
          "Любовь",
          "Материально-обеспеченная жизнь",
          "Наличие хороших друзей",
          "Уверенность в себе",
          "Познание",
          "Свобода как независимость",
          "Счастливая семейная жизнь",
          "Творчество"
        ],
        datasets: [
          {
            label: "Ценность",
            data:  [0, 7, 5, 9, 7, 4, 4, 8, 11, 2, 7, 2],
            backgroundColor: "transparent",
            borderColor: "rgba(1, 116, 188, 0.50)",
            pointBackgroundColor: "rgba(171, 71, 188, 1)"
          },
           {
            label: "Доступность",
            data:  [7, 7, 5, 10, 3, 2, 2, 7, 11, 2, 1, 9],
            backgroundColor: "transparent",
            borderColor: "rgba(1, 116, 188, 0.50)",
            pointBackgroundColor: "rgba(171, 71, 188, 1)"
          },
           {
            label: "Ценности-доступности",
            data:  [-7, 0, 0, -1, 4, 2, 2, 1, 0, 0, 6, -7],
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