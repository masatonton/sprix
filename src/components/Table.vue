<template>
  <v-simple-table fixed-header height="300px" style='margin:0vw 6vw;'  >
    <template v-slot:default>
      <thead>
        <tr>
          <th class="text-left">大会名</th>
          <th class="text-left">優勝</th>
          <th class="text-left">準優勝</th>
          <th class="text-left">ベスト４</th>
          <th class="text-left">ベスト４</th>
        </tr>
      </thead>
      <tbody>
        <tr v-for="item in desserts" :key="item.name">
          <td>{{ item.tonamel }}</td>
          <td>{{ item.vic }}</td>
          <td>{{ item.finalist }}</td>
          <td>{{ item.best41 }}</td>
          <td>{{ item.best42 }}</td>
        </tr>
      </tbody>
    </template>
  </v-simple-table>
</template>

<script>
  export default {
    data () {
      return {
        desserts: [
          {
            tonamel: 'Mythologia Championship vo.0',
            vic: 'アグネス',
            finalist:'たなか',
            best41:'てづか' ,
            best42:'てごし' ,
          },
        ],
      }
    },
  }
</script>