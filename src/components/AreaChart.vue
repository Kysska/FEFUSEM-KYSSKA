<script>
import { Line } from "vue-chartjs";

export default {
  extends: Line,
  data() {
    return {
      gradient: null,
      gradient2: null
    };
  },
  mounted() {
    this.gradient = this.$refs.canvas
      .getContext("2d")
      .createLinearGradient(0, 0, 0, 450);
    this.gradient2 = this.$refs.canvas
      .getContext("2d")
      .createLinearGradient(0, 0, 0, 450);

    this.gradient.addColorStop(0, "rgba(255, 0,0, 0.5)");
    this.gradient.addColorStop(0.5, "rgba(255, 0, 0, 0.25)");
    this.gradient.addColorStop(1, "rgba(255, 0, 0, 0)");

    this.gradient2.addColorStop(0, "rgba(0, 231, 255, 0.9)");
    this.gradient2.addColorStop(0.5, "rgba(0, 231, 255, 0.25)");
    this.gradient2.addColorStop(1, "rgba(0, 231, 255, 0)");

    this.gradient3.addColorStop(0, "rgba(0, 231, 255, 0.9)");
    this.gradient3.addColorStop(0.5, "rgba(0, 231, 255, 0.25)");
    this.gradient3.addColorStop(1, "rgba(0, 231, 255, 0)");

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
            borderColor: "#FC2525",
            pointBackgroundColor: "white",
            borderWidth: 1,
            pointBorderColor: "white",
            backgroundColor: this.gradient,
            data:  [0, 7, 5, 9, 7, 4, 4, 8, 11, 2, 7, 2]
          },
          {
            label: "Доступности",
            borderColor: "#05CBE1",
            pointBackgroundColor: "white",
            pointBorderColor: "white",
            borderWidth: 1,
            backgroundColor: this.gradient2,
            data: [7, 7, 5, 10, 3, 2, 2, 7, 11, 2, 1, 9]
          },
          {
            label: "Ценность-доступность",
            borderColor: "#e6aa88",
            pointBackgroundColor: "white",
            pointBorderColor: "white",
            borderWidth: 1,
            backgroundColor: this.gradient2,
            data: [-7, 0, 0, -1, 4, 2, 2, 1, 0, 0, 6, -7]
          }
        ]
      },
      { responsive: true, maintainAspectRatio: false }
    );
  }
};
</script>
