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

## vue-class-component & vue-property-decorator
* vuejs 에서 vue 컴포넌트를 클래스 스타일의 형태로 작성할 수 있게 별도 라이브러리를 제공한다.
  * 해당 라이브러리는 vue-class-component 이다.
* vue-class-component 를 계승해서, 별도의 다양한 데코레이터를 만드는게 그 라이브러리가 vue-property-decorator 이다.
* [vue-class-component](https://github.com/vuejs/vue-class-component)
* [vue-property-decorator](https://github.com/kaorun343/vue-property-decorator)

