<script>
export default {
  name: "Table",
  props: [
    'headers',
    'tableData',
    'title'
  ]
}
</script>

<template>
  <div>
      <h2>{{ title }}</h2>
      <table>
          <tr>
            <th v-for="header in headers">{{ header }}</th>
          </tr>
        <tr v-for="data in tableData">
          <td v-for="value in Object.values(data)">{{ value }}</td>
        </tr>
      </table>
    </div>
</template>

<style scoped>
table{
  border-collapse: collapse;
  border-radius: 0.75em;
  text-align: left;
  width: 50rem;
  box-shadow: 1em 1em 1em lightslategrey;
}
td, th{
  padding: 0.625em;
  border: 1px solid;
}

</style>