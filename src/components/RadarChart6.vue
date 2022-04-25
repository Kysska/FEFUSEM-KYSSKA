<script>
import { Radar } from "vue-chartjs";

export default {
  extends: Radar,
  mounted() {
    this.renderChart(
      {
        labels: [
          "Конфронтационный копинг",
          "Дистанцирование",
          "Бегство - избегание",
          "Принятие ответственности",
          "Положительная переоценка",
          "Планирование решения проблемы",
          "Самоконтроль",
          "Поиск социальной поддержки"
        ],
        datasets: [
          {
            label: "",
            backgroundColor: "rgba(179,181,198,0.2)",
            borderColor: "rgba(179,181,198,1)",
            pointBackgroundColor: "rgba(179,181,198,1)",
            pointBorderColor: "#fff",
            pointHoverBackgroundColor: "#fff",
            pointHoverBorderColor: "rgba(179,181,198,1)",
            data: [33, 83, 75, 83, 23, 44, 66, 22]
          }
        ]
      },
      { responsive: true, maintainAspectRatio: false }
    );
  }
};
</script>