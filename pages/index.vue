<template>
  <div>
    <v-text-field outlined label="filter" v-model="filter" @input="onChangeFilter"></v-text-field>
    <v-simple-table>
      <template v-slot:default>
        <thead>
          <tr>
            <th v-for="(key, index) in keys" :key="index" @click="onClickTh(key)">{{ key }}</th>
          </tr>
        </thead>
        <tbody>
          <tr v-for="(user, index) in users" :key="index">
            <td v-for="(key, index) in keys" :key="index">{{ user[key] }}</td>
          </tr>
        </tbody>
      </template>
    </v-simple-table>
  </div>
</template>

<script>
const originalUsers = require("~/assets/users.json");
export default {
  data() {
    return {
      originalUsers: originalUsers,
      users: originalUsers,
      filter: "",
      keys: ["name", "pref", "birthday", "score"]
    };
  },
  created() {},
  methods: {
    // <th>がクリックされたら呼ばれる
    onClickTh: function(key) {
      // this.usersをソートする
      console.log(key);
    },
    // filterの文字が変更されたら呼ばれる
    onChangeFilter: function() {
      // this.usersに絞り込んだ配列を入れる
      console.log(this.filter);
    }
  }
};
</script>