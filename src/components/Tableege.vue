 <template>
       <v-simple-table width = "300px" >
          <template v-slot:default>
      <thead>
        <tr>
          <th class="text-left">
            Название
          </th>
          <th class="text-left">
            Баллы
          </th>
        </tr>
      </thead>
      <tbody>
        <tr
          v-for="item in ege"
          :key="item.name"
        >
          <td>{{ item.name }}</td>
          <td>{{ item.ball }}</td>
        </tr>
      </tbody>
      </template>
  </v-simple-table>
    </template>
<script>
  export default {
    data () {
      return {
       ege: [
          {
            name: 'Русский язык',
            ball: 100,
          },
          {
            name: 'Биология',
            ball: 100,
          },
          {
            name: 'История',
            ball: 100,
          },
        ],
      }
    }
  }
  
</script>