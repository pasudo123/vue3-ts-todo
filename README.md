# vue3-ts-todo
* vue3
* typescript
* element plus

## 실행
```shell
$ npm run serve
```

## hot reload 동작안하는 경우
* `npm run serve --host localhost` 를 명령어로 처리한다.
* vue.config.js 파일에 아래와 같이 작성한다.
```js
module.exports = defineConfig({
  // devServer host 에 localhost 처리
  devServer: {
    host: 'localhost'
  }
})
```

## setup 사용방법
* https://vuejs.org/api/composition-api-setup.html
