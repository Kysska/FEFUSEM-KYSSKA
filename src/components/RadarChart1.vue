<script>
import { Radar } from "vue-chartjs";

export default {
  extends: Radar,
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
            label: "Ценности",
            backgroundColor: "rgba(179,181,198,0.2)",
            borderColor: "rgba(179,181,198,1)",
            pointBackgroundColor: "rgba(179,181,198,1)",
            pointBorderColor: "#fff",
            pointHoverBackgroundColor: "#fff",
            pointHoverBorderColor: "rgba(179,181,198,1)",
            data: [0, 7, 5, 9, 7, 4, 4, 8, 11, 2, 7, 2]
          },
        {
           label: "Доступности",
           backgroundColor: "rgba(255,99,132,0.2)",
           borderColor: "rgba(255,99,132,1)",
           pointBackgroundColor: "rgba(255,99,132,1)",
           pointBorderColor: "#fff",
           pointHoverBackgroundColor: "#fff",
           pointHoverBorderColor: "rgba(255,99,132,1)",
           data: [7, 7, 5, 10, 3, 2, 2, 7, 11, 2, 1, 9]
         },
         {
           label: "Ценность-доступность",
           backgroundColor: "rgba(255,99,132,0.2)",
           borderColor: "rgba(255,99,132,1)",
           pointBackgroundColor: "rgba(255,99,132,1)",
           pointBorderColor: "#fff",
           pointHoverBackgroundColor: "#fff",
           pointHoverBorderColor: "rgba(255,99,132,1)",
           data: [-7, 0, 0, -1, 4, 2, 2, 1, 0, 0, 6, -7]
         }
        ]
      },
      { responsive: true, maintainAspectRatio: false }
    );
  }
};
</script>