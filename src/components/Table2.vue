<template>
  <div class="hello">
    <h1>Welcome to the Table 2 page!</h1>
    <table id="table">
      <thead>
        <tr>
          <th>ID</th>
          <th>Username</th>
          <th>Last Login</th>
          <th>Login Count</th>
          <th>Project Count</th>
        </tr>
      </thead>
      <tbody>
        <tr v-for="item in data" v-bind:key="item.id">
          <td v-if="isGreen && item.login_count >= 1" style="background: green">{{ item.id }}</td>
          <td v-else style="background: white">{{item.id}}</td>
          <td v-if="isGreen && item.login_count >= 1" style="background: green">{{ item.username }}</td>
          <td v-else style="background: white">{{item.username}}</td>
          <td v-if="isGreen && item.login_count >= 1" style="background: green">{{ item.last_login }}</td>
          <td v-else style="background: white">{{item.last_login}}</td>
          <td v-if="isGreen && item.login_count >= 1" style="background: green">{{ item.login_count }} </td>
          <td v-else style="background: white">{{item.login_count}}</td>
          <td v-if="isGreen && item.login_count >= 1" style="background: green">{{ item.project_count }}</td>
          <td v-else style="background: white">{{item.project_count}}</td>
        </tr>
        <button v-on:click="isGreen = !isGreen"> Button </button>
      </tbody>
    </table>
  </div>
</template>

<script>
import json from "../../users.json"
export default {
  isGreen: false,
  name: 'Table2',
  data() {
    return {
        data: json,
        isGreen: false
    };
}
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>
#table {
  font-family: 'Open Sans', sans-serif;
  width: 750px;
  border-collapse: collapse;
  border: 3px 10px 0 10px;
}
table th {
  text-transform: uppercase;
  text-align: left;
  padding: 8px;
  min-width: 30px;
}
table td {
  text-align: left;
  padding: 8px;
  border-right: 2px solid #7D82A8;
  background: white;
}
table td:last-child {
  border-right: none;
}
table tbody tr:nth-child(2n) td {
  background: white;
}
button {
  text: bold;
  text-align: center;
  font-size: 20px;
  margin-top: 10px;
  padding: 20px;
  color: black;
  background: green;
  width: 100px;
  height: 5px;
}
</style>