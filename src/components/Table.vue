<template>
  <div class="hello">
    <h1>Welcome to Table 1 Page!</h1>
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
          <td v-if="isRed && item.login_count == 0" style="background: red">{{ item.id }}</td>
          <td v-else style="background: white">{{item.id}}</td>
          <td v-if="isRed && item.login_count == 0" style="background: red">{{ item.username }}</td>
          <td v-else style="background: white">{{item.username}}</td>
          <td v-if="isRed && item.login_count == 0" style="background: red">{{ item.last_login }}</td>
          <td v-else style="background: white">{{item.last_login}}</td>
          <td v-if="isRed && item.login_count == 0" style="background: red">{{ item.login_count }} </td>
          <td v-else style="background: white">{{item.login_count}}</td>
          <td v-if="isRed && item.login_count == 0" style="background: red">{{ item.project_count }}</td>
          <td v-else style="background: white">{{item.project_count}}</td>
        </tr>
        <button v-on:click="isRed = !isRed"> Button </button>
      </tbody>
    </table>
  </div>
</template>

<script>
// above in TR within THEAD could have dynamically added the same mapping to iterate and dynamiccaly add the items to the THEAD
import json from "../../users.json" // could have done a back end server response CRUD to send/ receive json data
export default {
  isRed: false,
  name: 'Table',
  data() {
    return {
        data: json, // if CRUD maybe add authentication - store session storage with key that is created from Redis then send to front end. When changing page request key to be verified with Redis and send page only when key === key if page is changed or its been 2 days kill key - re-authenticate. 
        isRed: false // Can store json data in server - better with NoSQL since it's formatted as Json anyways. Cross check person and key. 
    };
  }
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only 
Color would have been nice for background for full page
-->
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
  background: red;
  width: 100px;
  height: 5px;
}
</style>
