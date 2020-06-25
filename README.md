# sortable-table

## Build Setup

```bash
# install dependencies
$ npm install

# serve with hot reload at localhost:3000
$ npm run dev

# build for production and launch server
$ npm run build
$ npm run start

# generate static project
$ npm run generate
```

## 課題

* \<th\>がクリックされたらonClickThが呼ばれるので、その中でthis.usersをソートしてみよう
* filterの文字が更新されたらがonChangeFilterが呼ばれるので、その中でthis.usersを絞り込んでみよう

[pages/index.vue](pages/index.vue)
```
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
```

For detailed explanation on how things work, check out [Nuxt.js docs](https://nuxtjs.org).
